# Roadscript Studio — Feature Layers & Capabilities

Roadscript Studio is a creator-first authorship and provenance workspace.
It is **not** an image editor; it is a studio for **ownership, verification,
and lifecycle management** of visual media.

---

## Layer 0 — Invisible Watermark Core (Foundation)

> The cryptographic and signal-processing engine that powers all studio features.

### Capabilities
- Invisible watermark embedding with tunable robustness
- Reversible watermark payload encoding
- Irreversible (hash-based) watermark payload encoding
- Format-aware embedding (JPEG / PNG / TIFF / HEIF)
- Robust decoding under compression, resizing, and noise
- Deterministic embedding and verification
- Edge-case handling for low-texture and high-frequency images

---

## Layer 1 — Minimum Viable Studio (Authorship & Proof)

> Establishes Roadscript Studio as a system of record.

### Authorship Record Ledger
- Local, append-only authorship ledger
- Each entry includes:
  - Original image cryptographic hash
  - Watermarked image cryptographic hash
  - Embedded payload ID
  - Timestamp (creation and export)
  - Optional author, project, or series label
- No cloud dependency
- Human-readable + machine-readable storage

---

### Verification Report View
- Structured verification output
- Displays:
  - Decoded payload (raw + interpreted)
  - Integrity status (valid / altered / unknown)
  - Hash match results
  - Embedded vs detected timestamp
  - Confidence indicators
- Exportable formats:
  - PDF (human-facing)
  - JSON (machine-facing)

---

### Image Lifecycle View
- Visual lifecycle tracking:
- - Each state references ledger entries
- Enables traceability without visual editing

---

## Layer 2 — Creator Workflow Essentials (Non-Editing)

> Enables informed decisions without modifying image content.

### Pre-flight Image Inspector (Read-only)
- Displays:
- Resolution and aspect ratio
- Color space and bit depth
- Compression type and quality
- Metadata presence (EXIF/IPTC)
- Risk indicators:
- Platform recompression risk
- Color space conversion risk
- Watermark survivability estimate

---

### Export Intent Presets
> Presets define *intent*, not appearance.

- **Archival / Proof-of-Authorship**
- Maximum payload fidelity
- Low tolerance for destructive transforms

- **Social Media (Resilient)**
- Redundant embedding strategy
- Optimized for recompression and resizing

- **Client Delivery**
- Balanced robustness and reversibility
- Metadata compatibility prioritized

Each preset transparently documents:
- Payload redundancy level
- Channel usage strategy
- Expected survivability

---

### Semantic Batch Processing
- Batch operations grouped by:
- Project
- Platform
- Export intent
- Shared watermark configuration per batch
- Ledger entries linked at batch and file levels

---

## Layer 3 — Minimal Non-Destructive Image Operations

> Necessary transformations for real-world publishing.
> No creative manipulation.

### Non-Destructive Crop Presets
- **Platform Crop: Square (1:1)**
- **Platform Crop: Portrait (4:5)**
- **Platform Crop: Vertical Video (9:16)**
- **Proof Crop: Center-Safe**
- **No-Crop (Original Framing)**

All crops:
- Non-destructive
- Preview survivability impact before commit

---

### Resize Presets
- **Original Resolution**
- **Web Large (2048 px long edge)**
- **Web Standard (1080 px long edge)**
- **Platform Safe (Auto-detect)**
- **Custom Resolution**

Resize preview shows:
- Estimated watermark robustness change
- Platform compression risk warnings

---

### Safe Transform Simulator
- Predictive feedback before export:
- Compression survivability estimate
- Resize degradation impact
- Channel loss risk
- Color-coded risk indicators
- No hidden changes applied

---

## Layer 4 — Studio Differentiation (Authorship Infrastructure)

> Makes Roadscript Studio more than a tool — a trust layer.

### Authorship Certificate Generator
- Auto-generated certificate includes:
- Image preview
- Cryptographic hashes
- Embedded watermark summary
- Timestamp
- Verification instructions
- Export formats:
- PDF
- JSON

---

### Verification-Only Mode
- Decode and verify without embedding
- For:
- Clients
- Platforms
- Journalists
- Legal review
- No ledger modification allowed

---

### Future-Ready Integration Hooks (Inactive)
- C2PA compatibility pathway
- Platform-side verification APIs
- Camera-level embedding integration
- Hardware secure enclave support

Visible but disabled to signal roadmap intent.

---

## Explicit Non-Goals
- Full image editing
- Filters, LUTs, or color grading
- AI enhancement or retouching
- Social media scheduling
- Mandatory cloud accounts

Roadscript Studio focuses on **proof, provenance, and authorship** — not aesthetics.