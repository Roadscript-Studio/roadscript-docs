# Roadscript Studio License Model
## Feature Tiers
*Partial app license (free core features + paid advanced features)*  
The core features will be **free forever**  
Advanced features are **paid**, and implemented using feature flags  
Each license only works for **one major version**

---

Free features  
*They will be free forever*
- Basic watermark features: free (forever)
- Low strength payload: free (forever)
- Boolean verification: free (forever)
- Single image workflow: free (forever)  

--- 

Paid features
*A valid license needed, only works for **one major version***
- Reversible watermark: paid
- Cryptographic verification: paid
- Batch processing: paid
- Verification report (legal PDF document): paid
- Payload inspection: paid
- Export provenance data: paid

---

## License Tiers
Individual Free ($0.00)
- Basic invisible watermark
- Low-strength payload
- Boolean verification (pass / failed)
- Single-image workflow
- Local processing
- Project files

 Individual Pro ($12.99)
- High-strength watermark
- Reversible watermark
- Cryptographic verification
- Batch processing
- Verification PDF (legal format)
- Payload inspection
- Export provenance data
- Local-only operation
- Cross-platform (same generation)
- Intended for one individual

Creator Pro ($22.99)
- All Studio features
- Commercial / client delivery usage
- Use on client machines
- Client-facing verification reports
- Priority compatibility guarantees

Team License (Not available on iOS)
- All Studio features
- Multiple individuals
- Shared projects
- Team usage rights
- Centralized license scope

---

- Roadscript Studio uses a free core + paid professional feature model with generational licenses
- Paid licenses unlock advanced features and are valid across all supported platforms within the same major version. 
- Licenses are offered for individuals or studios, reflecting usage scale rather than specific devices.

---

## License Payload Structure (image license file)
A Roadscript license is a single .rsl file that also renders as a PNG certificate. The image is human-readable; the embedded license payload is machine-verifiable.
The license payload will consist of the following fields
- License header field: ROADSCRIPT-LICENSE
- License ID
- License type: Individual Pro / Creator Pro / Team License
- Major version number: e.g. version **1**.112
- Addon feature flags (still thinking)
- Owner ID: email address hash (SHA256)
- Signature: generated from a private key

---

## Local File Management
1. Each preset is organized into a project file, with input and output files, and configurations
2. Proof report will be in PDF format, and in legal structure
