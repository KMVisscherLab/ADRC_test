# MR-Guided PET Reconstruction and Duetto Processing

@[toc]()

## Component Overview

This component documents the UAB PET reconstruction workflow implemented through the internal MATLAB function:

```matlab
Unified_PET_Recon2(subjectID, PET_model_input, reconMode, varargin)
```

The function is located in the internal Cheaha project directory:

```text
/data/project/jonmc-lab/fang_collab/GE_toolbox/lmDuetto_v02.19.01_Aug2024/lmDuetto/runScripts-v8
```

The function and GE/Duetto software do **not** need to be uploaded to OSF. This component should contain only documentation, approved de-identified QC examples, parameter records, processing logs, and troubleshooting guidance.

## Purpose

The function provides one interface for three PET reconstruction modes:

1. **MR-Guided** — TOF-BSREM with T1, T2, or both priors; optional motion correction.
2. **Q.Clear** — standard TOF-BSREM; optional motion correction.
3. **Motion Only** — TOF-OSEM-PSF; optional motion correction.

## Supported PET Inputs

```text
PIB
TAU
FET
FMISO
```

The full paired-tracer, ZTE, and time-window logic is implemented for PiB, tau, FET, and FMISO.

## Internal Data Locations

```text
Raw data:
/data/project/jonmc-lab/fang_collab/GE_toolbox/RAW_DATA

GE/Duetto toolboxes:
/data/project/jonmc-lab/fang_collab/GE_toolbox

Final output:
/data/project/jonmc-lab/fang_collab/GE_toolbox/Processes_DATA_Final
```

## Workflow

```text
Raw PET/MR study
       |
       v
Copy study into a mode-specific processing directory
       |
       v
Sort DICOM and prepare Duetto-ready data
       |
       v
Check or recover ZTE/MRAC data
       |
       v
Select T1 and/or T2 prior
       |
       v
Use paired-tracer MR study when required data are missing
       |
       v
For MR-guided mode, create/find Q.Clear beta-300 PET reference
       |
       v
Register T1/T2/ZTE to PET reference
       |
       v
Run Duetto reconstruction
       |
       v
Write final DICOM output and preserve logs/run files
       |
       v
Perform registration and reconstruction QC
```

## Wiki Pages

0. home
1. Quick Start and Function Inputs
2. Reconstruction Modes and Parameters
3. Data Preparation, MR Priors, and Time Windows
4. Outputs, QC, and Troubleshooting
5. Code Safety Review and Handoff

## Restrictions

Do not upload GE Duetto software, proprietary support functions, raw list-mode data, identifiable DICOM files, MRAC data with protected information, credentials, or restricted subject outputs to OSF.
