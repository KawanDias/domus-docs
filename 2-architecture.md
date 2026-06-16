# 2. System Architecture

## 2.1 Architectural Overview

DOMUS is based on a hybrid multi-layer architecture that combines conventional web application infrastructure with blockchain verification mechanisms. The platform separates operational processing from immutable verification processes in order to balance scalability, maintainability, privacy, and security.

The architecture is divided into independent layers responsible for specific operational domains. This separation allows each component to evolve independently while maintaining clear communication boundaries across the system.

| Layer | Primary Responsibility | Purpose |
|---|---|---|
| Frontend Layer | User interaction | Provides interfaces for platform access |
| Backend Layer | Business logic and processing | Executes system operations and validations |
| Database Layer | Operational data storage | Stores platform information off-chain | 
| Blockchain Layer | Immutable verification | Registers cryptographic proof | 
| API Layer | Communication management | Connects system components securely | 

The platform adopts a hybrid architecture because storing all operational data directly on blockchain networks would increase operational costs, reduce scalability, and expose sensitive information publicly. DOMUS therefore uses blockchain selectively for integrity verification while maintaining conventional infrastructure for operational processing.

---

## 2.2 Frontend Layer

The frontend layer is responsible for all user interactions within the DOMUS platform. This layer provides the interfaces through which users access platform functionalities, submit information, monitor transactions, and interact with property-related data.

The frontend communicates with backend services through APIs and acts as the presentation layer of the system. Its primary objective is to provide a secure, accessible, and responsive interface for platform operations.

### Frontend Responsibilities

| Responsibility | Description |
|---|---|
| Property Visualization | Displays property listings and details | 
| Proposal Submission | Allows users to create proposals | 
| Transaction Monitoring | Tracks negotiation progress | 
| User Authentication | Manages login and session validation | 
Dashboard Interaction | Provides operational insights and controls | 

Depending on platform requirements, the frontend may be implemented through different interfaces.

| Interface Type | Status | 
|---|---|
| Web Application | Supported | 
| Mobile Application | Main platform focus | 
| Administrative Dashboard | Planned expansion | 

The frontend layer remains independent from blockchain operations. All blockchain communication occurs indirectly through backend services.

---

## 2.3 Backend Layer

The backend layer acts as the central processing unit of the DOMUS platform. This layer is responsible for business rule execution, transaction validation, blockchain communication, database management, and cryptographic verification processes.

The backend functions as an intermediary between operational infrastructure and blockchain networks. This separation prevents direct exposure of blockchain complexity to frontend applications while maintaining centralized control over validation and verification logic.


### Backend Responsibilities

| Component | Responsibility | 
|---|---|
| Business Logic Engine | Executes platform rules | 
| Validation Service | Verifies transaction consistency | 
| Hash Generator | Creates cryptographic transaction hashes | 
| Blockchain Service | Registers proofs on-chain | 
| Database Service | Stores operational records | 
| Authentication Service | Manages user validation |
| API Gateway | Coordinates external communication | 

The backend also manages error handling, request validation, authentication procedures, and system synchronization processes required for operational reliability.

---

## 2.4 Database Layer

The database layer is responsible for storing operational and transactional information required by the platform. DOMUS uses conventional database systems in order to preserve performance, scalability, and privacy while maintaining efficient access to system data.

Sensitive information remains stored off-chain because blockchain networks are not designed for high-volume confidential data storage. This approach reduces operational costs and improves data management flexibility.

### Stored Data

| Data Category | Description |
|---|---|
| User information | Account and profile records |
| Property Records | Property metadata and listings | 
| Proposal Details | Negotiation and offer information |
| Transaction History | Operational transaction logs |
| Payment Metadata | Payment-related references |

The database layer therefore functions as the primary operational storage infrastructure of the platform.

---

## 2.5 Blockchain Layer

The blockchain layer is responsible for immutable verification and auditability within the DOMUS architecture. Instead of storing complete transaction information publicly, the platform registers cryptographic hashes representing transaction states.

These blockchain records create immutable references capable of validating transaction integrity in future verification processes.

### Blockchain Responsabilities

| Function | Description |
|---|---|
| Hash Registration | Stores transaction hashes |
| Timestamp Validation | Provides chronological verification |
| Proof Storage | Maintains immutable references | 
| Integrity Validation | Detects unauthorized modifications |
| Event Immutability | Preserves historical consistency |

---

## 2.6 API Communication 

Communication between system components occurs through APIs. The API layer standardizes interactions between frontend interfaces, backend services, database systems, and blockchain integration modules. This structure improves interoperability and simplifies future integrations while maintaining centralized communication management.

The API layer is responsible for request validation, data formatting, authentication procedures, blockchain communication, and operational error handling. By centralizing communication logic through APIs, the platform maintains greater flexibility and improves the organization of internal services.

The communication flow also allows the frontend to reamain independent from blockchain complexity, since all blockchain interactions are handled indirectly through backend services.

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
This operational model creates a verifiable relationship between off-chain operational data and blockchain-registered proofs while preserving scalability and privacy.

---

## 2.8 Scalability Considerations

The architecture of DOMUS was designed to minimize unnecessary blockchain dependency. Instead of processing all operational information directly on-chain, the platform stores only cryptographic verification hashes on blockchain networks while maintaining operational logic within conventional infrastructure.

This architectural decision reduces gas costs, minimizes blockchain congestion, and decreases transaction latency. By limiting blockchain interactions to essential verification processes, the platform supports larger transaction volumes without depending entirely on blockchain performance limitations.

The hybrid infrastructure also allows independent scaling of backend services, databases, and frontend applications according to operational demand. This flexibility improves long-term maintainability and infrastructure adaptability.

---

## 2.9 Architectural Decisions

The architectural decisions adopted in DOMUS were designed to maintain efficiency, flexibility, maintainability, and compatibility with real-world operational requirements.

DOMUS also adopts modular system components. Each architectural layer operates independently and can evolve without requiring major structural modifications across the platform. This modularity simplifies maintenance procedures and supports future technological upgrades.

The platform also adopts API-based communication in order to standardize interactions between services and simplify future integrations. This approach improves system organization and reduces coupling between components.

---

## 2.10 Architectural Benefits

The proposed architecture provides operational, technical, and security-related benefits for the DOMUS platform. By combining conventional infrastructure with blockchain verification mechanisms, the system achieves efficient operational performance while maintaining strong integrity validation capabilities.

The architecture improves scalability by preserving most operational processing within traditional infrastructure while limiting blockchain usage to immutable verification operations. This approach reduces operational costs and avoids unnecessary blockchain congestion.

The modular organization of the system also simplifies maintenance, improves long-term adaptability, and facilitates future expansions. In addition, blockchain verification mechanisms strengthen transaction auditability and reduce risks associated with data modification.

Together, these architectural characteristics support the long-term sustainability, reliability, and scalability of the platform's digital real estate operations.
