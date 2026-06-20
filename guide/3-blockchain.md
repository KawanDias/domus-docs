# 3. Blockchain Integration

## 3.1 Blockchain Purpose
Blockchain technology is used within DOMUS as a verification and integrity assurance mechanism. The primary objective of blockchain integration is not to store complete transactional information, but rather to create immutable cryptographic proofs capable of validating the authenticity of transaction records.

By adopting this approach, DOMUS combines the efficiency of traditional infrastructures with the integrity guarantees provided by blockchain networks.

---

## 3.2 Why Blockchain Instead of Traditional Validation?
Traditional validation systems rely entirely on centralized databases controlled by a single organization. While these systems are efficient for operational processing, they introduce risks such as unauthorized modifications, internal manipulation, single points of failure, and limited historical auditability. 

Blockchain addresses these challenges by replacing centralized control and editable records with a decentralized infrastructure and distributed validation. This setup provides immutable, timestamped records that form a transparent audit trail, allowing completely independent integrity verification.

---

## 3.3 Cryptographic Hashing
Cryptographic hashing is the core verification mechanism used by DOMUS. A cryptographic hash function transforms data into a fixed-length output that acts as a unique digital fingerprint of the original information.

Any modification to the original data produces a completely different hash value. This characteristic allows the platform to detect unauthorized modifications by comparing newly generated hashes with previously registered blockchain records.

### Example
Original transaction data:
`Buyer + Seller + Property + Timestamp`

Generated hash: 
`a7f5f35426b927411fc9231b56382173...`

Even a minimal modification to the original transaction data results in a completely different output, making cryptographic hashes suitable for integrity verification.

---

## 3.4 Hashing Algorithms
Hashing algorithms are responsible for generating the cryptographic fingerprints used throughout the verification process. DOMUS may adopt industry-standard algorithms such as SHA-256 and Keccak-256, both widely used within blockchain ecosystems due to their reliability, security, and resistance to collisions.

These algorithms make it computationally impractical to reconstruct the original data from a generated hash and help ensure the consistency of verification records.

--- 

## 3.5 On-chain vs Off-chain Architecture
DOMUS follows a hybrid architecture that separates operational data from verification records. This design allows the platform to preserve privacy, reduce costs, and maintain scalability while still benefiting from blockchain verification.

Operational and sensitive information—including user records, property listings, financial details, proposal metadata, and internal logs—remains stored off-chain in conventional databases. Conversely, the blockchain network stores only the data required for validation, such as transaction hashes, verification timestamps, and smart contract events. The tradeoff is that the proof depends on the off-chain data remaining available; if it is lost, the on-chain proof alone proves nothing.

---

## 3.6 Smart Contracts
Smart contracts are autonomous programs deployed on blockchain networks that execute predefined logic deterministically without requiring direct human intervention. Within DOMUS, smart contracts are used to manage verification-related operations and blockchain registration processes.

These contracts may register transaction hashes, associate timestamps with verification events, manage proof records, and provide public validation endpoints to ensure consistency in verification procedures.

---

## 3.7 Verification Lifecycle
The verification lifecycle describes how transaction data becomes a blockchain-registered proof. This process establishes the relationship between operational records and blockchain validation data.

The lifecycle begins when a transaction is created or updated within the platform. The backend generates a cryptographic hash representing the transaction state and submits it to a smart contract. Once the blockchain network confirms the transaction, the verification record becomes permanent and available for future validation.

### Verification flow

```text
Transaction Creation
  ↓
Hash Generation
  ↓
Smart Contract Submission
  ↓
Blockchain Confirmation
  ↓
Immutable Verification Record
  ↓
Future Integrity Validation
```

---

## 3.8 Timestamp Validation
Timestamp validation is one of the features provided by blockchain networks. Every blockchain transaction is associated with a chronological record that indicates when a verification event occurred.

These timestamps provide evidence that specific information existed at a particular moment and allow events to be reconstructed in chronological order. This capability is useful during audits, compliance reviews, and legal or financial disputes where event sequencing must be independently verified.

---

## 3.9 Network Selection
Blockchain network selection directly impacts operational costs, transaction speed, scalability, and security. DOMUS considers networks like Ethereum, which offers robust security and high decentralization but introduces higher gas fees, and Polygon, which provides lower operational costs and faster confirmations despite a slightly lower level of decentralization.

Polygon is currently considered a strong candidate due to its balance between scalability, performance, and reduced transaction costs. However, the final network selection may vary according to future operational requirements.

---

## 3.10 Gas Optimization
Gas fees represent the operational costs associated with blockchain transactions. Because each on-chain operation incurs a gas fee, DOMUS adopts strategies designed to minimize on-chain operations.

Following the hybrid design (3.5), the platform optimizes these costs by reducing transaction payload sizes and prioritizing efficient smart contract design. Future implementations may also support batch processing techniques when appropriate.

---

## 3.11 Blockchain Limitations
Despite its benefits, blockchain technology introduces operational constraints such as transaction fees, network congestion, scalability limitations, and dependency on network availability.

DOMUS mitigates these constraints by leveraging the hybrid architecture split (3.5).

---

## 3.12 Key Benefits of Integration
Together, cryptographic hashing (3.3), on-chain proof registration (3.6), and blockchain timestamps (3.8) give DOMUS tamper-evident, independently auditable transaction records without exposing operational data.
