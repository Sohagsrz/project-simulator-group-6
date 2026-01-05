# Implemented Features
## T1: layout marchant login screen
marchant page design 
**status : implemented**

## T2: Design DB Schema (Users, Auth)

Create database models for user accounts, roles, and authentication.
Define relationships, constraints, and indexes for efficient queries.
Plan tables for both personal users and merchants.

**Status : Implemented**

## T4: Setup Express.js Server Routing.

Implemented modular Express.js routing architecture with feature-based route separation and middleware support to ensure scalable REST API development during the sprint.

**Status : Implemented**

## T5: Build "Bank Account Mock" API

Developed a mock banking service simulating balance checks, debit/credit, and OTP verification to enable safe testing of transaction flows without real bank integration.

**Status : Implemented**

## T6: Full Banking & Transaction Engine

Implemented end-to-end banking and transaction features including a mock bank API (debit/credit/balance with OTP), modular Express routing, transaction DB schema (audit-ready), instant transfer engine (Bank ↔ MFS) with validation and fees, Payment & Request Money APIs using JWT auth, mock MFS adaptors (bKash, Nagad, Rocket), daily settlement scheduler, partial refund logic with rollbacks, and Jest unit tests for core flows.

**Status : Implemented**

## T7: Design Transaction DB Schema

Designed a normalized MongoDB/SQL schema for transactions with sender, receiver, amount, status, and timestamps.

Structured database to support auditability, refunds, and settlements.

Ensured data integrity and compliance with financial record-keeping standards.

**Status : Implemented**

## T8: Implement "Instant Transfer" Engine

Built real-time transaction engine for Bank ↔ MFS transfers.

Added validation, fee calculation, and atomic DB updates.

Ensured fast, secure, and reliable fund transfers.

**Status : Implemented**

## T9: Build "Payment" & "Request Money" APIs

Developed RESTful APIs for sending payments and requesting money.

Used JWT authentication and secure transaction handling.

Ensured consistent behavior for peer-to-peer and merchant transactions.

**Status : Implemented**

## T10: Integrate Mock MFS Adaptors

Integrated mock MFS adaptors (bKash, Nagad, Rocket) for testing.

Created standardized interfaces for provider-agnostic transactions.

Enabled end-to-end simulation of wallet operations without real accounts.

**Status : Implemented**

## T11: Build "Daily Settlement" Scheduler

Implemented cron-based scheduler for automatic merchant payouts.

Monitored transaction status and generated logs for settlements.

Ensured timely and accurate fund transfers to linked bank accounts.

**Status : Implemented**

## T12: Implement "Partial Refund" Logic

Developed partial refund functionality with amount validation.

Used transaction rollback to maintain consistency in MongoDB/SQL.

Ensured secure and accurate fund reversal for disputed payments.

**Status : Implemented**