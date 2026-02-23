# GemminAI | Deterministic Geopolitical Intelligence Engine

> **Current Integrity Status: 49/49 PASS** > All analytical layers are cryptographically signed and verified via JCS (JSON Canonicalization Schema).

## 1. Positioning

GemminAI is a **deterministic geopolitical intelligence engine**. Determinism is achieved through canonicalized JSON serialization, fixed-weight scoring functions, and cryptographic signatures. Unlike standard LLM implementations, GemminAI transforms volatile OSINT data into verifiable, multi-perspective intelligence artifacts.

### Key Functional Pillars

- **Structured OSINT Ingestion**: Automated harvesting of high-signal geopolitical data.
    
- **Multi-model Delta Variance Analysis**: Cross-referencing independent LLM architectures (Gemini, Claude, GPT) to identify narrative outliers.
    
- **Canonicalized Output**: Standardization of JSON structures using **JCS (RFC 8785)** to ensure bit-perfect reproducibility.
    
- **Cryptographic Integrity Verification**: Every analytical artifact is hashed and signed using industry-standard curves.
    
- **Temporal Drift Detection**: Drift is computed across consecutive snapshots captured three times daily from live OSINT feeds.
    

---

## 2. Core Concepts

### Conflict Fragility Index (CFI)

CFI quantifies the tension between competing global narratives.

$$CFI = \text{mean}(\text{variance across WEST / GLOBAL / EAST lenses})$$

### Narrative Drift

Drift measures the instability and evolution of a specific topic over a temporal axis.

$$\text{Drift} = w_1\Delta CFI + w_2\text{SemanticShift} + w_3\text{ModelVariance}$$

---

## 3. Deterministic Integrity Layer

To ensure that intelligence artifacts remain untampered, GemminAI implements a strict security pipeline:

1. **JSON Canonicalization (JCS)**: Eliminates non-deterministic formatting (RFC 8785).
    
2. **SHA-256 Hashing**: Generates a unique digital fingerprint of the data.
    
3. **ECDSA (P-256) Digital Signatures**: Provides non-repudiation of the source.
    
4. **Integrity Seal**: If a single bit mismatches, the engine refuses to render the content.
    

---

## 4. Architecture
```
OSINT Data Source → Harvester → Structured Schema (JSON)
                         ↓
             Delta Variance Analysis (Multi-Model) → Global Synthesis
                         ↓
             Canonicalization (JCS) → SHA-256 Hash
                         ↓
              ECDSA (P-256) Signature → UI / API Output
```

---
## 5. Verification & Reproducibility

To ensure the system itself has not been tampered with, we provide the **Official Implementation Hash** for the core verification script.

### Official Implementation Hash (v1.0.0)
|**Component**|**SHA-256 Hash**|
|---|---|
|`src/verify_integrity.py`|`3a5a3a9d1b13367621b5b34cc25a0d886a7da39ef91015a3f757ae37908602b8`|

To verify the system integrity:
```
shasum -a 256 src/verify_integrity.py
```

**To reproduce and verify the artifacts:**

1. **Run Harvester**: Fetch raw data from defined OSINT feeds.
    
2. **Generate Structured Artifact**: Pass data through the multi-model analysis pipeline.
    
3. **Canonicalize JSON**: Normalize the output using the JCS engine.
    
4. **Hash & Sign**: Generate the SHA-256 hash and apply the ECDSA signature.
    
5. **Verify**: Use the public key to confirm the artifact has not been tampered with

---
## 6. Vision

This project demonstrates how structured intelligence artifacts can be made **reproducible, verifiable, and temporally analyzable**. By bridging the gap between Large Language Models and cryptographic security, GemminAI establishes a new standard for "Digital Acta Diurna" — where truth is protected by mathematics.

© 2026 Gemmina Intelligence LLC.

---
