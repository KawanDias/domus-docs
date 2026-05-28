# 2. System Architecture

## 2.1 Architectural Overview

DOMUS is based on a hybrid multi-layer architecture combining traditional web application components with blockchain verification systems.

The architecture is divided into:

- Frontend Layer
- Backend Layer
- Database Layer
- Blockchain Layer

This separation improves modularity, scalability, and maintainability.

---

## 2.2 Frontend Layer

The frontend layer is responsible for all user interactions.

### Main responsabilities:

- Property visualization
- Proposal submission
- Transaction monitoring
- User authentication
- Dashboard interaction

The interface may be implemented as:

- Web application 
- Mobile application (MAIN)
- Administrative dashboard (MAYBE)

--- 

## 2.3 Backend Layer

The backend acts as the core processing unit of the system,

### Responsabilities include:

- Business rule execution
- Transaction validation
- Hash generation
- API communication
- Blockchain interaction
- Database management

The backend also acts as an intermediary between off-chain and on-chain operations.

---

## 2.4 Database Layer

Traditional databases are used to store operational information.

### Stored data includes:

- User information
- Property records
- Proposal details
- Transaction history
- Payment metadata

Sensitive data remains off-chain for privacy and performance reasons.

---

## 2.5 Blockchain Layer

The blockchain layer ius reponsible for immutable verification.

### Main functions:

- Hash registration
- Timestamp validation
- Verification proof storage
- Event immutability

No sensitive transaction data is stored publicly.

---

## 2.6 API Communication 

Communication between system components occurs through APIs.

### API responsabilities:

- Request validation
- Data formatting
- Authentication
- Blockchain communication
- Error handling

---

## 2.7 Data Flow

The operational flow follows the sequence below:

1. User initiates an action
2. Frontend sends request to backend
3. Backend validates information
4. Hash is generated
5. Blockchain transaction is executed
6. Verification record is stored
7. Confirmation returned to user

---

## 2.8 Scalability Considerations

The architecture minimizes blockchain dependency by storing only verification hashes on-chain.

This reduces:

- Gas costs
- Blockchain congestion
- Transaction latency

---

## 2.9 Architectural Decisions

Several design decisions were adopted to maintain system efficiency.

### Off-chain Storage
Used to optimize performance and privacy.

### Modular Components 
Each layer can evolve independently.

---

## 2.10 Architectural Benefits

The proposed architecture provides:

- Lower operational costs (VERY IMPORTANT)
- Better scalability
- Enhanced integrity
- Easier maintenance
- Improved security

  
