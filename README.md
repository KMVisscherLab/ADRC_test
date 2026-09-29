
# 🧠 Multimodal Imaging & Biomarker Study Protocols

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.placeholder.svg)](https://zenodo.org/)
![NIH Funding](https://img.shields.io/badge/NIH-Supported-blue)
![HIPAA Notice](https://img.shields.io/badge/Data_Safety-No_PII-red)

> **Principal Investigator:** [PI Name]  
> **Study Contact:** [Lab Manager / Coordinator Email]  
> 
> ⚠️ **CONFIDENTIALITY NOTICE:** This repository contains study protocols, Standard Operating Procedures (SOPs), and pipeline code. **No Protected Health Information (PHI) or participant identifiable data is stored here.**

---

## 🧭 Fast Navigation Guide for Study Staff
Click any of the **[View Protocol]** links in the tables below to open and read or print the standard operating procedures. 

---

## 📋 1. Before the Scan (Recruitment & Intake)
Participant identification, registry screening, consenting procedures, and MRI/PET visit scheduling.

| Protocol / SOP | Study Track | Format | Link |
| :--- | :--- | :--- | :--- |
| **Participant Recruitment** | ADRC Cohort | 📄 Word Doc | [View Protocol](an/recruitment-adrc.docx01-before-the-scan/recruitment-adrc.docx) |
| **Participant Recruitment** | CLARITI Cohort | 📄 Word Doc | [View Protocol](01-before-the-scan/recruitment-clariti.docx) |
| **Enrollment, Consenting & Scheduling** | All Participants | 📄 Word Doc | [View Protocol](01-before-the-scan/enrollment-consenting-scheduling.docx) |

---

## ⏱️ 2. During the Scan (Acquisition Protocols)
Scanner console setup, radiotracer administration timelines, and acquisition SOPs.

| Protocol Name | Modality / Tracer | Format | Link |
| :--- | :--- | :--- | :--- |
| **Amyloid Imaging Protocol** | Amyloid PET / MRI | 📄 Word Doc | [View Protocol](02-during-the-scan/amyloid-scan-protocol.docx) |
| **PiB PET Protocol** | [11C]-PiB PET | 📄 Word Doc | [View Protocol](02-during-the-scan/pib-pet-protocol.docx) |

---

## 🔄 3. After the Scan (Preprocessing & Data Storage)
Initial image quality checks, standardized preprocessing for open data sharing, and long-term repository uploads.

### A. Pre-Processing for Data Sharing

| Pipeline Step | Focus Area | Link |
| :--- | :--- | :--- |
| **SUIT Cerebellar Processing** | Cerebellar isolation & PET reference region normalization | [View Guide](03-after-the-scan/preprocessing-for-sharing/suit-cerebellar-processing-reference-regions.md) |
| **Blazer Workflow** | Automated processing and quality control pipeline | [View Guide](03-after-the-scan/BLAzER.md) |
| **MR-Guided PET Reconstruction** | Anatomically constrained PET reconstruction | [View Guide](03-after-the-scan/preprocessing-for-sharing/mr-guided-pet-reconstruction.md) |


### B. Data Storage & Repository Management

| Resource | Target System | Link |
| :--- | :--- | :--- |
| **Summary of Storage Contents** | Local / Cloud Tiers | [View Storage Manifest](03-after-the-scan/data-storage/storage-summary-manifest.md) |
| **SCAN / DVCID & LONI Archiving** | LONI / External Repositories | [View Archiving SOP](03-after-the-scan/data-storage/scan-dvcid-and-loni-archiving.md) |

---

## 📊 4. Dataset Processing & Analytics
Secondary pipelines, biomarker quantification, and downstream structural analyses.

| Processing Stream | Description | Link |
| :--- | :--- | :--- |
| **White Matter Hyperintensity (WMH)** | Lesion segmentation, volumetric extraction, and scripts | [View Pipeline & Code](04-dataset-processing/whitematter-hyperintensity-pipeline.md) |

---

## 🩺 5. Clinical Safety & Monitoring
Clinical oversight and management protocols for scan-related incidental findings.

| Clinical SOP | Indication | Format | Link |
| :--- | :--- | :--- | :--- |
| **Standard of Care for ARIA** | ARIA-E / ARIA-H Monitoring & Escalation | 📄 Word Doc | [View Protocol](05-clinical/aria-standard-of-care.docx) |

---

## ℹ️ Archiving & Citation
To cite these study workflows in publications or progress reports:
```bibtex
@misc{study_protocols_2026,
  title  = {Multimodal Imaging Protocols and Processing Pipelines},
  author = {[PI and Key Personnel]},
  year   = {2026},
  doi    = {10.5281/zenodo.placeholder}
}
