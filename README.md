
# 🧠 UAB ADRC Multimodal Imaging & Biomarker Study Protocols 🧠 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.placeholder.svg)](https://zenodo.org/)
![NIH Funding](https://img.shields.io/badge/NIH-Supported-blue)
![HIPAA Notice](https://img.shields.io/badge/Data_Safety-No_PII-red)

> **This document is meant for two purposes: First, to serve as a quick reference for identifying and organizing information needed for the project during performance of the project.  Second, it will serve as documentation of the protocols used as part of this project.**
>  
> 
> ⚠️ **CONFIDENTIALITY NOTICE:** This repository contains study protocols, Standard Operating Procedures (SOPs), and pipeline code. **No Protected Health Information (PHI) or participant identifiable data is stored here.**

---

## 🧭 Overview
For an overview of the processes that lead up to participants in our study undergoing imaging, please see ***Chad's flowchart** 
Click any of the **[View Protocol]** links in the tables below to open and read or print the standard operating procedures. \

To suggest changes to this document, please email Kristina Visscher. 
Contact information for the people described here are listed in this password protected document: XXXXlink to box fileXXXX. 



---

## 📋 1. Before the Scan (Recruitment & Intake)
Participant identification, registry screening, consenting procedures, and MRI/PET visit scheduling.

| Protocol / SOP | Study Track | Format | Link |
| :--- | :--- | :--- | :--- |
| **Participant Recruitment** | ADRC Cohort | 📄 Word Doc | [View Protocol](an/recruitment-adrc.docx01-before-the-scan/recruitment-adrc.docx) |
| **Participant Recruitment** | CLARITI Cohort | 📄 Word Doc | [View Protocol](01-before-the-scan/recruitment-clariti.docx) |
| **Enrollment, Consenting & Scheduling** | All Participants | 📄 Word Doc | [View Protocol](01-before-the-scan/enrollment-consenting-scheduling.docx) |

### Scheduling
* Schedules for the PET MRI are in a password protected calendar here: ###link to uabmc calendar### (you will need your uabmc credentials to view)
* Scheduling for the PET MRI depends on time slots available, along with tracer production.  More information about that is here XXbox folderXXXXX
* 
---

## ⏱️ 2. During the Scan (Acquisition Protocols)
Imaging Data are collected on "Amyloid Day" and "Tau Day".
### Tau Day: 
* Possible PET tracers include: XXXXXX
* [Manual of Procedures](02-during-the-scan/tau-MOP.docx) are detailed explanations of the set of procedures, including radiotracer administration timelines 
* [Participant Information Sheets](02-during-the-scan/tau-PI.docx) are forms that include checklists for during-scan acquisition and places for notes during the scan.

### Amyloid Day: 
* Possible PET tracers include: XXXXXX
* [Manual of Procedures](02-during-the-scan/amy-MOP.docx) are detailed explanations of the set of procedures, including radiotracer administration timelines 
* [Participant Information Sheets](02-during-the-scan/amy-PI.docx) are forms that include checklists for during-scan acquisition and places for notes during the scan.

### Data Uploads:
* DESCRIBE THE PROCESS OF UPLOADING THE IMAGING DATA, BOTH PET AND MRI (PERHAPS LINK TO DOCUMENT)
* DESCRIBE WHERE THE OTHER DATA, INCLUDING REDCAP, GOES (PERHAPS LINK TO DOCUMENT)

For questions about scan acquisition, contact: Dean Fang for science-based PET questions, Kristina Visscher for science-based MRI questions, Denise Jeffers for questions about tracer production, Tyler Stamps for participant wrangling.
---

## 🔄 3. After the Scan (Preprocessing & Data Storage)
Initial image quality checks, standardized preprocessing for open data sharing, and long-term repository uploads.

### A. Pre-Processing for Data Sharing

**Describe the process that Mohammad goes through to do a first pass analysis of the dataset.
**Describe the hand off from Mohammad to Deepak and Vee to get the dataset ready for further review and upload to SCAN. [maybe this is a link to a word document?]

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
```
