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

## T13: Write Unit Tests for Core Logic

Wrote unit tests using Jest for all core backend flows.

Verified transaction engine, refunds, and settlements for correctness.

Reduced regression risks and ensured backend reliability.

**Status : Implemented**


## T15: Initialize Git & Project Structure

Set up the Git repository and branch strategy (main, dev, feature branches).

Organize the project folder structure for backend, frontend, configs, and docs.

Ensure consistent coding standards and linting.

**Status : Implemented**

## T16: Build Login/Register API (JWT)

Implement REST APIs for user registration and login.

Use JWT (JSON Web Token) for secure session management.

Include password hashing, input validation, and error handling.

**Status : Implemented**

## T17: Middleware: Rate Limiting & Validation

Implement middleware to prevent abuse and limit request frequency.

Add input validation middleware to ensure all API requests meet expected formats.

**Status : Implemented**

## T18: Integrate Biometric Auth Hooks

Set up hooks for biometric authentication (e.g., Face ID, Touch ID) on supported devices.

Integrate with login or sensitive transaction verification.

**Status : Implemented**

## T19: Setup Notifications System (Firebase)

Integrate Firebase Cloud Messaging (FCM) to send real-time notifications.

Notifications include successful transactions, payment requests, or alerts.

**Status : Implemented**

## T20: Implement "Forgot Password" Email Flow

Build secure password reset mechanism via email.

Generate token-based links with expiry, validate tokens, and update passwords.

**Status : Implemented**

## T21: Global Error Logging Service

Implement centralized error logging for backend services.

Capture exceptions, API failures, and user-facing errors for debugging.

**Status : Implemented**

## T22: Security Audit & Penetration Testing

Perform security checks on APIs, database, and authentication flows.

Identify vulnerabilities like SQL injection, XSS, or insecure data storage.

Apply fixes and harden the system against attacks.

**Status : Implemented**
## T23 : Layout Login/Signup Screens
Design the authentication screens including login and registration forms with proper input fields, validation hints, error messages, and smooth user navigation.

**Status : Implemented**

## T24  : Design Figma Prototypes (Merchant App)  
Create high-fidelity Figma designs for the merchant application focusing on usability and consistency.
Ensure screens follow branding guidelines and support smooth merchant workflows.

**Status : Implemented**

## T25  : Merchant Login Screen Layout
Design and implement the merchant login interface with input validation and clean UI.
Ensure secure access and user-friendly navigation for merchants.

**Status  : Implemented**

## T26  : Merchant Dashboard Skeleton
Develop the basic structure of the merchant dashboard to display key metrics and actions.
Prepare placeholders for earnings, QR payments, analytics, and transaction summaries.

**Status  : Implemented**

##  T27:  Generate QR Code Feature
Implement dynamic QR code generation for merchant payment acceptance.
Ensure QR codes are secure, scannable, and linked to merchant transaction data.

**Status  : Implemented**

## T28  : Add Cashier Interface
Build an interface that allows merchants to add, manage, and assign cashiers.
Support role-based access to ensure controlled transaction handling.

**Status  : Implemented**

## T29  : Withdraw Earnings Function
Develop functionality enabling merchants to withdraw earnings to linked bank or MFS accounts.
Ensure transaction validation, confirmation, and error handling.

**Status  : Implemented**

##  T30  : Upload Inventory CSV Feature
Implement CSV upload functionality for bulk inventory management.
Validate file format and store product data securely in the system

**Status  : Implemented**

##  T31  : Sales Analytics using Chart.js
Integrate Chart.js to visualize merchant sales performance and trends.
Display daily, weekly, and monthly insights for better business decisions.
**Status  :  Implemented**

##  T32  : Send Invoice Email Tool
Develop an email-based invoice generation and sending feature for merchants.
Ensure invoices include transaction details and are delivered securely.
**Status  :  Implemented**
