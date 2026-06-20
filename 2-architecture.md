# 2. System Architecture

## 2.1 Architectural Overview
DOMUS is based on a hybrid multi-layer architecture that combines conventional web application infrastructure with blockchain verification mechanisms. The platform separates operational processing from immutable verification processes in order to balance scalability, maintainability, privacy, and security.

The architecture is divided into independent layers responsible for specific operational domains. This separation allows each component to evolve independently while maintaining clear communication boundaries across the system.

The platform adopts a hybrid architecture because storing all operational data directly on blockchain networks would increase operational costs, reduce scalability, and expose sensitive information publicly. DOMUS therefore uses blockchain selectively for integrity verification while maintaining conventional infrastructure for operational processing.

---

## 2.2 Frontend Layer
The frontend layer is responsible for all user interactions within the DOMUS platform. This layer provides the interfaces through which users access platform functionalities, submit information, monitor transactions, and interact with property-related data.

The frontend communicates with backend services through APIs and acts as the presentation layer of the system. Its primary objective is to provide a secure, accessible, and responsive interface for platform operations.

Through these interfaces, users browse property listings and their details, create and submit proposals, monitor the progress of ongoing negotiations, authenticate and manage their sessions, and reach operational controls through a dashboard.

Depending on platform requirements, the frontend may be implemented through different interfaces, focusing primarily on a mobile application with supported web access and planned administrative expansions.

---

## 2.3 Backend Layer
The backend layer acts as the central processing unit of the DOMUS platform. The backend runs the platform's business rules, validates transactions for consistency, generates the cryptographic hashes that represent transaction states, registers those proofs on-chain, persists operational records to the database, authenticates users, and coordinates external communication through an API gateway.

The backend also manages error handling, request validation, authentication procedures, and system synchronization processes required for operational reliability.

---

## 2.4 Database Layer
The database layer is responsible for storing operational and transactional information required by the platform. DOMUS uses conventional database systems in order to preserve performance, scalability, and privacy while maintaining efficient access to system data.

Sensitive information remains stored off-chain because blockchain networks are not designed for high-volume confidential data storage. This approach reduces operational costs and improves data management flexibility.

The database stores user account and profile records, property metadata and listings, proposal and offer details, operational transaction logs, and payment-related references.

The database layer therefore functions as the primary operational storage infrastructure of the platform.

---

## 2.5 Blockchain Layer
The blockchain layer is responsible for immutable verification and auditability within the DOMUS architecture. Instead of storing complete transaction information publicly, the platform registers cryptographic hashes representing transaction states.

These blockchain records create immutable references capable of validating transaction integrity in future verification processes.

The blockchain layer registers transaction hashes, timestamps them for chronological verification, and stores them as immutable proofs. Later checks compare against these records to detect unauthorized modifications and preserve a consistent history.

---

## 2.6 API Communication
Communication between system components occurs through APIs. The API layer standardizes interactions between frontend interfaces, backend services, database systems, and blockchain integration modules. This structure improves interoperability and simplifies future integrations while maintaining centralized communication management.

The API layer is responsible for request validation, data formatting, authentication procedures, blockchain communication, and operational error handling. By centralizing communication logic through APIs, the platform maintains greater flexibility and improves the organization of internal services.

---

## 2.7 Data Flow
The operational flow of DOMUS follows a structured sequence designed to maintain validation consistency and integrity verification throughout transaction processing.

The process begins when a user initiates an action through the frontend interface. The frontend sends the request to the backend, where transaction data is validated according to business rules and operational requirements. After validation, the backend generates a cryptographic hash representing the relevant transaction state.

The generated hash is then registered on a blockchain network as an immutable verification proof. Once the blockchain transaction is completed, the verification record is stored within the platform and a confirmation is returned to the user.

```text
User
  ↓
Frontend Layer
  ↓
Backend Validation
  ↓
Hash Generation
  ↓
Blockchain Registration
  ↓
Verification Record Storage
  ↓
User Confirmation
```

---

## 2.8 Architectural Benefits
Together, the hybrid split (2.1), modular layering, and on-chain verification (2.5) give DOMUS scalable operations with tamper-evident auditability.
