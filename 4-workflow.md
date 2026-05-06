# 4. Operation Workflow

## 4.1 Overview 

The transaction process in DOMUS is divided into key stages, each recorded though blockchain verification.

---

## 4.2 Property Listing

- Seller registers a property
- Data stored off-chain

(No blockchain interactions at this stage)

---

## 4.3 Proposal Creation

- Buyer submits a proposal
- System generates hash of proposal data
- Hash is stored on blockchain

---

## 4.4 Seller Acceptance

- Seller accepts proposal
- New hash generated including acceptance data
- Recorded on blockchain

--- 

## 4.5 Payment Registration

- Payment occurs off-chain (e.g., PIX, bank transfer)
- Payment proof is hashed
- Hash stored on blockchain

---

## 4.6 Transaction Finalization

- Final transaction summary is generated
- Final hash created and stored

---

## 4.7 Audit Process

At any time:

- System recalculates hash
- Compares with blockchain record

If mismatch → data was altered

---

## 4.8 Key Advantage

This workflow ensures:

- End-to-end traceability
- Tamper detection
- Transparent verification








































