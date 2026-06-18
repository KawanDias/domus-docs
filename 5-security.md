# 5. Security

## 5.1 Security Overview

Security within DOMUS is based on a combination of conventional application security practices and blockchain-based verification mechanisms. The objective is to protect transaction records, preserve data integrity, and provide reliable methods for detecting unauthorized modifications.

Rather than relying exclusively on blockchain technology, the platform adopts a layered security approach. Traditional infrastructure remains responsible for authentication, authorization, and operational data management, while blockchain mechanisms provide independent verification of critical transaction records.

---

## 5.2 Cryptographic Hashing

Cryptograhic Hashing is one of the primary security mechanisms used within DOMUS. Hash functions transform transactions data into fixed-lenght outputs that act as digital fingerprints of the original information.

These hashes are generated from relevant transaction records and subsequently registered on the blockchain. Because hash functions are deterministic, the same input always produces the same output, while any modification to the original data results in a completely different hash value.

This characteristic allows the platform to verify whether stored information remains consistent with previously registered verification records.

---

## 5.3 Data Integrity

Data integrity refers to the ability to ensure that information remains unchanged after it has been recorded. Within DOMUS, integrity verification is performed through the comparison of current transaction data against blockchain-registered cryptographic proofs.

When a verification process is executed, the platform recalculates the hash associated with a transaction and compares it to the corresponding blockchain record. Matching values indicate that the information remains consistent with the original registration, while differences indicate that the data has been modified since the proof was created.

This process allows unauthorized modifications to be detected without exposing sensitive transaction information.

---

## 5.4 Immutability 

Immutability is one of the security properties provided by blockchain networks. Once a verification record has been confirmed and included in the blockchain, it becomes extremely difficult to alter without compromissing the underlying network consensus mechanisms.

Within DOMUS , immutability applies to the cryptographic proofs registered on-chain rather than to the operational data itself. This distinction allows the platform to preserve the flexibility of conventional databases while maintaining permanent verification references for audit and validation purposes.

As a result, historical verification records remain available as long-term evidence of previous transaction states

---

## 5.5 Transparency and Auditability 

Transparency and auditability are achieved through the use of publicly verifiable blockchain records. Because verification proofs are stored on a blockchain network, they can be independently validated without requiring direct access to the platform's internal infrastructure.

This capability supports audit processes by allowing transaction records to be compared against immutable verification references. It also reduces dependence on a single source of trust when evaluating the authenticity of historical records.

The transparency provided by this model applies to verification data only. Sensitive operational information remains protected within the platform infrastructure.

---

## 5.6 Fraud Prevention

DOMUS incorporates security mechanisms designed to reduce risks associated with unauthorized data modification and record manipulation. By maintaining immutable verification proofs, the platform makes it significantly easier to identify discrepancies between stored information and previously registered transaction states. 

These mechanisms help detect attempts to alter records after verification events have ocurred. They also strengthen the reliability of transaction histories by providing evidence that specific transaction states existed at a particular point in time.

Although blockchain verification improves resistance to manipulation, it should be understood as a verification mechanism rather than a complete fraud prevention solution.

---

## 5.7 Security Model

The security model adopted by DOMUS combines multiple layers of protection that operate together throughout the transaction lifecycle.

Traditional infrastructure is responsible for authentication, access control, database protection, and operational security procedures. Blockchain technology complements these mechanisms by providing independent verification of transaction records through cryptographic proof registration.

This hybrid model allows the platform to balance security, privacy, operational efficiency, and long-term maintainability while avoiding unnecessary dependence on blockchain infrastructure.

---

## Security Limitations

No security architecture can eliminate all possible risks. While blockchain verification provides strong guarantees regarding the integrity of registered records, it cannot determine whether the original information submitted to the platform was accurate or intentionally misleading.

The effectiveness of verification processes therefore depends on the quality and legitimacy of the data recorded during transaction events. In addition, blockchain verification does not prevent fraud that occurs entirely outside the platform environment.

For this reason, blockchain-based validation should be viewed as one component of a broader security strategy that also includes operational controls, legal procedures, and responsible user behavior.












































