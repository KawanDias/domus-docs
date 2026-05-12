# 3. Blockchain Integration

## 3.1 Blockchain Purpose

Blockchain techology is used within DOMUS as a verification and integrity assurance mechanism.

The primary objective of blockchain integration in not to store complete transactional information, but rather to create immutable cryptographic proofs capable of validating the authenticity of transaction records.

This approach allows the platform to combine the efficiency of traditional infrastructures with the security guarantees provided by decentralized systems.

---

## 3.2 Why Blockchain Instead of Traditional Validation?

Traditional systems rely entirely on centralized databases controlled by single entities.

Although efficient for operational purposes, centralized architectures present risks such as:

- Unauthorized data modification
- Internal manipulation
- Single points of failure
- Difficulty proving historical authenticity

Blockchain introduces characteristics capable of mitigating these issues:

- Immutability
- Distributed validation
- Transparent auditing
- Timestamped records
- Tamper resistance

DOMUS leverages these characteristics to estabilish trust in transaction verification processes.

---

## 3.3 Cryptographic Hashing

The core verification mechanism used by DOMUS is cryptographic hashing.

A hash function transforms data into a fixed-size string that acts as a unique digital fingerprint.

### Example

Original transaction data:

Buyer + Seller + Property + Timestamp

Generated output: 

a7f5f35426b927411fc9231b56382173...

Even minimal modifications in the original data generate completely different hashes.

---

## 3.4 Hashing Algorithms

DOMUS may use secure cryptographic algorithms such as:

- SHA-256
- Keccak-256

These algorithms are widely adopted in blockchain infrastructures due to their collision resistance and integrity guarantees.

---

## 3.5 On-chain vs Off-chain Architecture

DOMUS follows a hybrid architecture.

## Off-chain Data

Stored in traditional databases>

- User information
- Property records
- Financial data
- Proposal details
- Internal metadata

### On-chain Data

Stored on blockchain networks:

- Transaction hashes
- Verification timestamps
- Smart contract events

This strategy reduces costs while preserving privacy.

---

## 3.6 Smart Contracts

Smart contracts are autonomous programs deployed on blockchain networks.

Within DOMUS, smart contracts may be responsible for:

- Registering hashes
- Associating timestamps
- Managing verification events
- Providing public validation endpoints

---

## 3.7 Verification Lifecycle

The blockchain verification process follows multiple stages.

### Step 1 - Transaction Creation

The platform generates or updates transaction data.

### Step 2 - Hash Generation

The backend generates a cryptographic hash from the transaction payload.

### Step 3 - Blockchain Registration

The hash is sent to the blockchain through a smart contract transaction.

### Step 4 - Confirmation

After network validation, the hash becomes immutable.

### Step 5 - Future Verification

The platform may recalculate hashes and compare them with blockchain records.

--- 

## 3.8 Timestamp Validation

Blockchain transactions naturally generate timestamps.

These timestamps provide:

- Chronological verification
- Proof of existence
- Historical ordering

This feature is particularly important in legal or financial disputes.

---

## 3.9 Network Selection

DOMUS may operate an blockchain network such as:

### Ethereum

Advantages: 
- High decentralization
- Strong security

Disadvantages:
- High gas fees

### Polygon
- Lower operational costs
- Faster confirmations

Disadvantages:
- Slightly lower decentralization

Polygon is considered a strong candidate due to its scalability and reduced fees.

---

### 3.10 Gas Optimization

Blockchain operations generate costs commonly know as gas fees.

DOMUS minimizes costs through:

- Minimal on-chain storage
- Reduced transaction payloads
- Batch processing possibilities
- Efficient smart contract design

---

## 3.11 Blockchain Limitations

Despite its benefits, blockchain technology also presents limitations.

### Main limitations include:

- Transaction fees
- Network congestion
- Scalability restrictions
- Dependency on internet connectivity

DOMUS addresses these limitations by using blockchain only as a verification layer.

---

# 3.12 Key Benefits of Integration

The integration model adopted by DOMUS provides:

- Tamper detection
- Immutable verification
- Transparent auditing
- Increased trust
- Reduced manipulation risks




































