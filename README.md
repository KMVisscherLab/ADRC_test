# 🧠 UAB ADRC Multimodal Imaging & Biomarker Study Protocols 🧠

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.placeholder.svg)](https://zenodo.org/)
![NIH Funding](https://img.shields.io/badge/NIH-Supported-blue)
![HIPAA Notice](https://img.shields.io/badge/Data_Safety-No_PII-red)

> **Document Purpose:** 
> 1. Serve as a quick reference for identifying and organizing information needed during active study performance.
> 2. Document and standardize protocols across the project. 
> 
> *Links to this repository will be posted on the front page of the MOPs in the PET/MRI suite for easy access.*

> [!WARNING]
> **CONFIDENTIALITY NOTICE:** This repository contains study protocols, Standard Operating Procedures (SOPs), and pipeline code. **No Protected Health Information (PHI) or participant identifiable data is stored here.**

<br>

## 🧭 Overview

* **Workflow Flowchart:** For an overview of the processes leading up to participant imaging, please see **Chad's Flowchart** *(link pending)*.
* **Document Maintenance:** To suggest changes or updates to this documentation, please email Kristina Visscher.
* **Internal Directory:** Contact information for study personnel is listed in this password-protected [UAB Box Document](https://uab.app.box.com/file/2495951435335) *(ensure access permissions are set for project collaborators)*.

<hr style="height: 4px; background: #0969da; border: none; margin: 48px 0 32px 0; border-radius: 2px;" />

<h2 style="background-color: #f0f4f9; border-left: 6px solid #0969da; padding: 12px 16px; border-radius: 0 6px 6px 0; margin-bottom: 20px;">📋 1. Before the Scan (Recruitment & Intake)</h2>

Participant identification, registry screening, consenting procedures, and MRI/PET visit scheduling.

### SOPs & Protocols

| Protocol / SOP | Study Track | Format | Link |
| :--- | :--- | :---: | :--- |
| **Participant Recruitment** | ADRC Cohort | 📄 Word Doc | [View Protocol](01-before-the-scan/recruitment-adrc.docx) |
| **Participant Recruitment** | CLARITI Cohort | 📄 Word Doc | [View Protocol](01-before-the-scan/recruitment-clariti.docx) |
| **Enrollment, Consenting & Scheduling** | All Participants | 📄 Word Doc | [View Protocol](01-before-the-scan/enrollment-consenting-scheduling.docx) |

### Scheduling Logistics
* **PET/MRI Calendar:** Access the master schedule via the password-protected [UABMC Calendar](link-placeholder) *(UABMC credentials required)*.
* **Slot & Tracer Coordination:** Scheduling depends on scanner slot availability and radiotracer synthesis timing. Detailed coordination workflows are stored in the [Tracer Production & Scheduling Box Folder](link-placeholder).

<hr style="height: 4px; background: #0969da; border: none; margin: 48px 0 32px 0; border-radius: 2px;" />

<h2 style="background-color: #f0f4f9; border-left: 6px solid #0969da; padding: 12px 16px; border-radius: 0 6px 6px 0; margin-bottom: 20px;">⏱️ 2. During the Scan (Acquisition Protocols)</h2>

> [!NOTE]
> Imaging data are collected across two separate visits: **Amyloid Day** and **Tau Day**.

### Tau Day
* **Tracers:** Possible PET tracers include `XXXXXX`
* **MOP:** [Manual of Procedures](02-during-the-scan/tau-MOP.docx) – Detailed procedural steps and radiotracer administration timelines.
* **Forms:** [Participant Information Sheets](02-during-the-scan/tau-PI.docx) – Checklists and real-time acquisition notes.

### Amyloid Day
* **Tracers:** Possible PET tracers include `XXXXXX`
* **MOP:** [Manual of Procedures](02-during-the-scan/amy-MOP.docx) – Detailed procedural steps and radiotracer administration timelines.
* **Forms:** [Participant Information Sheets](02-during-the-scan/amy-PI.docx) – Checklists and real-time acquisition notes.

### 📤 Data Uploads
* Describe the process of uploading imaging data (both PET and MRI).
* Describe where peripheral and clinical data (e.g., REDCap) are stored.

### 👥 Scan Acquisition Contacts

| Role | Contact Person | Responsibility |
| :--- | :--- | :--- |
| **PET Operations** | Dean Fang | Scientific PET protocol & sequence questions |
| **MRI Operations** | Kristina Visscher | Scientific MRI sequence & imaging questions |
| **Radiochemistry** | Denise Jeffers | Tracer production and delivery timelines |
| **Participant Handling** | Tyler Stamps | Participant scheduling and suite wrangling |

<hr style="height: 4px; background: #0969da; border: none; margin: 48px 0 32px 0; border-radius: 2px;" />

<h2 style="background-color: #f0f4f9; border-left: 6px solid #0969da; padding: 12px 16px; border-radius: 0 6px 6px 0; margin-bottom: 20px;">🔄 3. After the Scan (Preprocessing & Data Storage)</h2>

Initial image quality checks, standardized preprocessing for open data sharing, and long-term repository uploads.

### A. Pre-Processing for Data Sharing

* **Initial QA / First Pass:** Describe the process that Mohammad goes through to do a first-pass analysis of the dataset.
* **Handoff Workflow:** Describe the handoff from Mohammad to Deepak and Vee to get the dataset ready for further review and upload to SCAN *(link to SOP / Word doc pending)*.

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

<hr style="height: 4px; background: #0969da; border: none; margin: 48px 0 32px 0; border-radius: 2px;" />

<h2 style="background-color: #f0f4f9; border-left: 6px solid #0969da; padding: 12px 16px; border-radius: 0 6px 6px 0; margin-bottom: 20px;">📊 4. Dataset Processing & Analytics</h2>

Secondary pipelines, biomarker quantification, and downstream structural analyses.

| Processing Stream | Description | Link |
| :--- | :--- | :--- |
| **White Matter Hyperintensity (WMH)** | Lesion segmentation, volumetric extraction, and scripts | [View Pipeline & Code](04-dataset-processing/whitematter-hyperintensity-pipeline.md) |

<hr style="height: 4px; background: #0969da; border: none; margin: 48px 0 32px 0; border-radius: 2px;" />

<h2 style="background-color: #f0f4f9; border-left: 6px solid #0969da; padding: 12px 16px; border-radius: 0 6px 6px 0; margin-bottom: 20px;">🩺 5. Clinical Safety & Monitoring</h2>

Clinical oversight and management protocols for scan-related incidental findings.

| Clinical SOP | Indication | Format | Link |
| :--- | :--- | :---: | :--- |
| **Standard of Care for ARIA** | ARIA-E / ARIA-H Monitoring & Escalation | 📄 Word Doc | [View Protocol](05-clinical/aria-standard-of-care.docx) |

<hr style="height: 4px; background: #0969da; border: none; margin: 48px 0 32px 0; border-radius: 2px;" />

<h2 style="background-color: #f6f8fa; border-left: 6px solid #57606a; padding: 12px 16px; border-radius: 0 6px 6px 0; margin-bottom: 20px;">ℹ️ Archiving & Citation</h2>

To cite these study workflows in publications or progress reports:

```bibtex
@misc{study_protocols_2026,
  title  = {UAB ADRC Multimodal Imaging Protocols and Processing Pipelines},
  author = {[UAB ADRC Staff]},
  year   = {2026},
  doi    = {10.5281/zenodo.placeholder}
}
