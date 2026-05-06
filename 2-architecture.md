# 2. System Architecture

## 2.1 Overview

DOMUS follows a layered architecture composed of three main components:

- Frontend Layer
- Backend Layer
- Blockchain Layer

## 2.2 Frontend Layer

Responsible for user interaction, including:

- Property listing visualization
- Proposal submission
- Transaction tracking

Technologies may include web or mobile frameworks.

## 2.3 Backend Layer

Handles:

- Business logic
- Data storage
- API communication
- Hash generation

The backend acts as the bridge between the application and the blockchain.

## 2.4 Blockchain Layer

Used exclusively for:

- Storing transaction hashes
- Ensuring immutability
- Enabling public verification

No sensitive or raw data is stored on-chain.

## 2.5 Data Flow

1. User performs an action (e.g., creates proposal)
2. Backend processes data
3. Hash is generated
4. Hash is sent to blockchain
5. Transaction is recorded immutably

## 2.6 Design Principles

- Minimal on-chain data
- High integrity
- Low operational cost
- Scalability







































































