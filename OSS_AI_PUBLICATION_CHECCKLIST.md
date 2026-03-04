# Open-Sourcing Foundational AI Models & Systems  
*A Practical Guide for Professors in AI Research*

If your research focuses on foundational AI models and systems, your open-source strategy should balance:

- 📄 Academic citation & reproducibility  
- 🧪 Research transparency  
- 🏗 Long-term infrastructure sustainability  
- ⚖ Licensing/IP protection  
- 🌍 Community adoption  

---

# 1️⃣ Define What You Are Releasing

For foundational AI research, you may release:

- [ ] Model training code  
- [ ] Inference code  
- [ ] Model weights (if permitted)  
- [ ] Evaluation scripts  
- [ ] Experiment configurations  
- [ ] Dataset processing pipeline  
- [ ] Distributed training or serving infrastructure  

You **do not need to release everything**. Many labs release:
- Code + configs + checkpoints  
- But not raw datasets (due to licensing constraints)

---

# 2️⃣ Standard Academic Open-Source Workflow

## Step A — Primary Development Repository

**Platform:**  
- **GitHub** (organization: GitHub, software hosting platform)

**Best Practices:**
- Public repo at submission (or private until camera-ready)
- Include:
  - [ ] Clear README
  - [ ] Installation instructions
  - [ ] Minimal reproducible example
  - [ ] Citation BibTeX
  - [ ] LICENSE file
  - [ ] Model Card
  - [ ] Reproducibility script

---

## Step B — Archival & DOI (For Citation)

**Platform:**  
- **Zenodo** (organization: Zenodo, research archiving platform)

**Why Use It:**
- Generates DOI
- Archives exact release version
- Often required by funders

**Workflow:**
1. Connect Zenodo to GitHub
2. Create a GitHub release (e.g., v1.0)
3. Zenodo automatically mints a DOI
4. Cite the DOI in your paper

This ensures long-term preservation independent of GitHub.

---

## Step C — Model Distribution & Community Adoption

If releasing model weights:

**Platform:**  
- **Hugging Face** (organization: Hugging Face, AI model hosting platform)

**Advantages:**
- Model cards (technical + ethical documentation)
- Dataset hosting
- Built-in evaluation tracking
- Download metrics
- Pull requests from community
- Easy integration with the Transformers ecosystem

Typical structure used by major labs:

- GitHub → code  
- Hugging Face → model weights  
- Zenodo → archival DOI  

---

# 3️⃣ Long-Term Infrastructure Governance (Optional)

If your system becomes infrastructure-level software:

**Organization:**
- **Linux Foundation** (nonprofit tech consortium)
- **LF AI & Data** (Linux Foundation AI umbrella)

Example hosted projects:
- ONNX (Open Neural Network Exchange)
- ONNX Runtime
- OpenLineage

Consider this route if:
- You expect industry contributors  
- You want neutral governance  
- You anticipate enterprise adoption  
- You want long-term sustainability  

This is typically a **post-publication step**, not pre-submission.

---

# 4️⃣ Licensing Strategy (Critical)

## Permissive Licenses (Common in Research)

- MIT
- Apache 2.0 (recommended for research systems)

**Apache 2.0 advantages:**
- Includes patent protection
- Industry-friendly
- Widely adopted in AI systems research

---

## Model-Specific Licenses

For foundation models:
- Custom Responsible AI licenses
- OpenRAIL-style licenses (common in Hugging Face ecosystem)

Be careful about:
- Dataset license compatibility  
- Institutional IP policies  
- Funding agency requirements  
- Export control (especially for large models)

---

# 5️⃣ Recommended Open-Source Stack for AI Professors

| Purpose | Platform |
|----------|----------|
| Development | GitHub |
| Archival DOI | Zenodo |
| Model Weights | Hugging Face |
| Dataset Hosting | Hugging Face Datasets |
| Long-Term Governance | Linux Foundation (optional) |
| Preprint | arXiv + GitHub link |

---

# 6️⃣ What Major AI Labs Typically Do

Structural patterns (not endorsements):

- OpenAI → selective release strategy  
- Meta AI → GitHub + custom model licenses  
- Stanford CRFM → GitHub + Hugging Face  
- EleutherAI → GitHub + HF + community governance  

---

# 7️⃣ Professional Release Checklist

## Legal
- University tech transfer approval  
- Funding compliance (NSF/DOE/etc.)  
- Dataset redistribution rights  
- Export control review  

## Technical
- Remove credentials and secrets  
- Clean commit history  
- Dockerfile or Conda environment  
- Automated evaluation scripts  
- Hardware requirements documented  

## Documentation
- Model Card  
- System architecture diagram  
- Limitations section  
- Responsible AI statement  
- Intended use & misuse cases  

---

# 8️⃣ Strategic Phased Approach

## Phase 1 — Publication Stage
- GitHub repository  
- Zenodo DOI  

## Phase 2 — Community Adoption
- Hugging Face model page  
- Demo or inference endpoint  

## Phase 3 — Infrastructure Maturity
- Consider Linux Foundation incubation  
- Formal governance structure  
- Technical steering committee  

---

# 9️⃣ Optional: Lab-Wide Open-Source Policy

If you publish frequently, consider creating:

- Standard LICENSE template  
- Standard Model Card template  
- Standard reproducibility checklist  
- Default repository structure  
- Governance guidelines for large collaborative projects  
