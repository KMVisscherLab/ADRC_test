# SUIT–FreeSurfer Hybrid Cerebellar Processing

@[toc]()
![SUIT–FreeSurfer hybrid cerebellar segmentation](https://osf.io/download/cxdtp/)



## Component Overview

This component documents the SUIT–FreeSurfer hybrid cerebellar processing workflow used to create subject-specific cerebellar reference regions for downstream PET analysis.

The workflow is implemented in the MATLAB function:

`create_suit_freesurfer_hybrid_final(subjID, fsDir, suitRepoDir, qcDir)`

The code is stored in the following UAB Box folder:

https://uab.app.box.com/folder/404673369390

The workflow is applied after FreeSurfer structural processing. It registers a cerebellar anatomical atlas from MNI space to the individual subject's FreeSurfer space, combines the warped SUIT information with the subject's `aparc+aseg.mgz`, preserves the standard FreeSurfer labels outside the cerebellar gray matter, and replaces the original cerebellar cortical labels with two new labels:

- `3000`: inferior cerebellar gray-matter candidate region
- `3001`: remaining cerebellar gray matter

The resulting hybrid atlas can be used in later PET SUV or SUVR extraction, with or without partial-volume correction. This step is independent of PET partial-volume correction and independent of fMRIPrep.

## Main PET Applications

### PiB amyloid PET

For the current PiB pipeline, the reference region is the **whole cerebellum**.

In the hybrid output, a whole-cerebellum mask can be formed from:

```text
7    Left cerebellar white matter
46   Right cerebellar white matter
3000 Inferior cerebellar gray matter
3001 Remaining cerebellar gray matter
```

Therefore:

```text
PiB whole cerebellum = labels 7 + 46 + 3000 + 3001
```

The standard Centiloid PiB method uses the whole cerebellum as its reference region. The exact target mask, image space, smoothing, and Centiloid calibration method must remain consistent with the approved analysis protocol.

### Tau PET

For flortaucipir tau PET, the intended reference region is **inferior cerebellar gray matter**.

In the current hybrid atlas, label `3000` is intended to provide this region:

```text
Tau inferior cerebellar gray matter = label 3000
```

Inferior cerebellar gray matter is commonly used for cross-sectional flortaucipir SUVR analysis. However, reference-region choice can affect cross-sectional and longitudinal results, so the selected region must be documented and used consistently.

## Important Current Validation Status

The function has produced a visually successful cerebellar overlay in the tested subject example.

Before label `3000` is treated as a final inferior cerebellar gray-matter reference region across the full cohort, the atlas label list and resulting anatomy must be confirmed against the exact SUIT lookup table included in `suitRepoDir`.

The current code includes SUIT labels `33` and `34` in the inferior mask. In the standard Diedrichsen anatomical atlas, labels `29–34` correspond to deep cerebellar nuclei rather than cerebellar cortical lobules. Although the FreeSurfer cerebellar-gray-matter intersection may remove most of these voxels, labels `33` and `34` should be reviewed and normally excluded when the scientific goal is a pure cerebellar cortical gray-matter reference region.

## Workflow Position

```text
T1-weighted MRI
      |
      v
FreeSurfer processing
      |
      v
brain.mgz + aparc+aseg.mgz
      |
      v
Register MNI template to subject T1 with SynthMorph
      |
      v
Warp SUIT atlas to subject FreeSurfer space
      |
      v
Intersect SUIT regions with FreeSurfer cerebellar gray matter
      |
      v
Create labels 3000 and 3001
      |
      v
Save hybrid aparc+aseg atlas
      |
      v
Visual QC
      |
      +------------------------------+
      |                              |
      v                              v
PiB whole-cerebellum SUVR       Tau inferior-GM SUVR
(labels 7,46,3000,3001)         (label 3000 after validation)
```

## Main Output

```text
<fsDir>/<subjID>/mri/SUIT_Segment/aparc+aseg_wInfGM.nii.gz
```

This volume retains the original FreeSurfer segmentation outside the cerebellar cortical gray matter while replacing FreeSurfer labels `8` and `47` with the new cerebellar labels.

## Component Pages

1. **Home** — Overview and PET reference-region use
2. **Inputs Setup and Execution** — Required files, software, Cheaha, and local execution
3. **Registration and Hybrid Atlas Logic** — Complete algorithm and label definitions
4. **PET Reference Regions** — PiB whole cerebellum and tau inferior cerebellar gray matter
5. **Quality Control and Troubleshooting** — Visual QC, validation checks, and failures
6. **Code Review and Handoff** — Required improvements, outputs, and completion checklist

## Data Security

Do not upload identifiable MRI or PET data, DICOM files containing protected health information, credentials, or restricted participant-level results to OSF.

Only approved code, documentation, lookup tables, de-identified examples, and approved QC images should be uploaded.
