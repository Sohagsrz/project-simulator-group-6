# Simulation Plan — feature/build-bank-acc

Purpose: Describe non-code simulation scenarios to validate the banking and transaction features described in `PROJECT_FEATURES.md` without writing production code.

Overview: For each feature below, the simulation describes inputs, expected behaviour, and verification steps.

1) Express.js Server Routing
- Simulation: Simulate API request flowcharts and trace logs for route resolution.
- Input: HTTP method + path examples (e.g., POST /api/v1/payments).
- Expected: Correct middleware order (auth → validation → handler) and logged request metadata.
- Verify: Walk through example traces and confirm middleware sequence.

2) Bank Account Mock API
- Simulation: Mock bank user with starting balance; simulate debit, credit, balance inquiries, and OTP flow.
- Input: Debit 100.00, OTP correct/incorrect; Credit 50.00.
- Expected: Debit reduces balance only after OTP success; credit increases immediately.
- Verify: Balance before/after table and OTP attempt logs.

3) Transaction DB Schema
- Simulation: Sample transaction records (sender, receiver, amount, status, timestamps) for create, settle, refund.
- Input: Create payment $120, partial refund $30.
- Expected: New transaction record with status=completed; refund creates linked record and updates balances in audit trail.
- Verify: Schema fields present, referential link between original and refund records.

4) Instant Transfer Engine (Bank ↔ MFS)
- Simulation: Sequence diagram for transfer flow (validation, fee calc, debit, credit, atomic commit).
- Input: Bank → MFS transfer $200, fee 1.5%.
- Expected: Sender debited $203.00 (incl. fee), receiver credited $200.00; single atomic operation or compensating rollback on failure.
- Verify: Transaction states across steps and error-handling paths.

5) Payment & Request Money APIs
- Simulation: Authenticated request flows using JWT; scenarios: P2P payment, merchant payment, money request and accept.
- Input: JWT with user id; POST /payments $45; POST /requests $75 then accept.
- Expected: Authorization check passes, transactions created with correct metadata, request becomes payment on acceptance.
- Verify: Request lifecycle and permission checks in simulated logs.

6) Mock MFS Adaptors (bKash, Nagad, Rocket)
- Simulation: Provider-agnostic adaptor interface; emulate provider latency, success/failure responses, and idempotency keys.
- Input: Transfer via `bKash` adapter with network timeout.
- Expected: Retry/backoff behaviour simulated; idempotent handling prevents duplicate debits.
- Verify: Adapter response table and retry traces.

7) Daily Settlement Scheduler
- Simulation: Cron run that collects merchant transactions, computes payouts, and marks settled status.
- Input: Batch of merchant transactions for one day totaling $5,000.
- Expected: Payout instructions generated, ledger entries created, settlements marked with timestamp.
- Verify: Settlement report with totals, fees, and per-merchant payout records.

8) Partial Refund Logic
- Simulation: Refund eligibility checks, validation of refund amount, and rollback path for failed refund.
- Input: Original payment $100, request partial refund $40.
- Expected: Refund record created, balances updated, original transaction updated to show partial refund metadata.
- Verify: Consistency checks and rollback trace if DB update fails in the middle.

9) Unit Test Scenarios (Jest-style descriptions)
- Simulation: Plain-language test cases for core logic: transfer success/failure, fee calc, OTP verification, refund edge cases.
- Example test: "should not debit on failed OTP" — Input debit+incorrect OTP; Expect no balance change.

How to use these simulations
- Create example data tables and sequence diagrams (drawn or in docs) to walk through flows.
- Run manual scenario checklists, record inputs/outputs, and use the results to guide later code implementation.

Deliverables in this branch: this `SIMULATIONS.md` file (non-code) describing all scenarios.

Status: Draft — ready for your review and edits.
