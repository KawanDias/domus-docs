# 4. Operational Workflow

## 4.1 Overview

The operational workflow of DOMUS defines how transaction events are processed, validated, and recorded throughout the platform. Each stage produces records that contribute to the overral traceability of the transaction lifecycle.

---

## 4.2 Property Listing

The workflow begins when a seller registers a property within the platform. During this stage, property information is stored in the platform databse and becomes available for consultation by potential buyers.

No blockchain interaction occurs at this stage because the property listing process does not yet represent a transactional commitment between parties. The information remains entirely within the operational infrastructure of the platform.

---

## 4.3 Proposal Creation

The proposal creation stage begins when a buyer submits an offer for a listed property. The proposal data is processed by the backend and recorded within the platform database.

Once the proposal has been created, the system generates a cryptographic hash representing the proposal state. This hash is registered on the blockchain as a verification record, creating evidence that the proposal existed in a specific form at a particular moment.

---

## 4.4  Seller Acceptance

The seller acceptance stage occurs when the property owner formally accepts a proposal submitted through the platform. This action changes the transaction state and creates a new verification event.

The backend generates a new cryptographic hash that includes the updated transaction information. This hash is subsequently registered on the blockchain, creating a new immutable proof associated with the acceptance event.

The backend generates a new cryptographic hash that includes the updated transaction information. This hash is subsequently registered on the blockchain, creating a new immutable proof associated with the acceptance event.

---

## 4.5 Payment Registration

The payment registration stage records evidence that the financial component of the transaction has been completed. The payment itself occurs outside the blockchain environment through conventional payment methods such as bank transfers or PIX transactions.

After payment confirmation, the platform generates a cryptographic hash derived from the payment evidence or related transaction records. This hash is then registered on the blockchain as part of the verification history.

---

## 4.6 Transaction Finalization

The transaction finalization stage marks the conclusion of the negotiation process. At this point, the platform generates a final transaction summary containing the information required to represent the completed state of the operation.

A final cryptograhic hash is generated and recordeed on the blockchain. This record becomes the definitive verification reference associated with the completed transaction.

---

## 4.7 Audit Process

The audit process allows previously recorded transactions to be validated at any point in time. During a verification procedure, the platform recalculates the hash associated with the stored transaction data and compares the result against the corresponding blockchain record.

If both values match, the transaction data remains consistent with the information originally registered. If the values differ, the verification process indicates that be stored data no longer corresponds to the blockchain proof and should be investigated.

### Workflow Summary

```text
Property Listing
        ↓
Proposal Creation
        ↓
Seller Acceptance
        ↓
Payment Registration
        ↓
Transaction Finalization
        ↓
Audit and Verification
```

---

## 4.8 Key Advantage

The workflow adopted by DOMUS establishes a verifiable record of important transaction events without requiring sensitive operational information to be stored on-chain.

By combining conventional transaction processign with blockchain-based proof registration, the platform improves traceability and simplifies future verification procedures. This approach enables transaction states to be independently validated while maintaining the efficiency and privacy of traditional infrastructure.
























