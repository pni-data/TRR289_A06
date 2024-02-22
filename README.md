# TRR289 A06

## ℹ️ Information
*This repository is the Github sibling of the corresponding [DataLad](https://www.datalad.org/) dataset, i.e. it **does not** contain the data itself.*
The GitHub sibling, nevertheless, provides insights into the general data structure (directory tree, filenames) and serves as a starting point to download, share and discuss the dataset.
 Data is in BIDS format and may include behavioral, questionnaire and derivative data, too.
Data is stored in a special S3 remote provided by [Coscine](https://coscine.rwth-aachen.de/) and can't be downloaded without the dataset specific secret token.
Token is available at project Z03 for members of TRR289 and collaborators upon reasonable request.

See `dataset_description.json` for project related meta-data.

## ⬇️ How to download dataset

#### 1. Install it with DataLad based on the github handle
This does not download the actual data, only the gin-annex "skeleton".
```bash
datalad install -s git@github.com:pni-data/<dataset_name>.git <dataset_name>
```
#### 2. Set up the security token to access the actual data
Token is available at project Z03 for members of TRR289 and collaborators upon reasonable request.
```bash
export AWS_ACCESS_KEY_ID="XXXXX-XXXX-XXXX-XXXX-XXXX"
export AWS_SECRET_ACCESS_KEY="XXXXXXXX"
```

#### 2. Change to the dataset directory and download the file(s) you want
You can selectively download what you need (e.g. derivatives only).
```bash
cd <dataset_name>
datalad get <path/to/file*>
```


See our [documentation](https://github.com/pni-data/.github/blob/master/profile/README.md) for more detail.

Comments added by the SFB289 Z03 project coordinators
====================================================================

General Comments
--------------------------------------------------------------------
ToDo:

description of the dataset,including link to the openly available SFB proposal/some publication
eg: This dataset was acquired by the team of the SFB289 XX project. It includes YY subjects and the common sequences within the SFB289 project, namely a high resolution T1w, resting state fMRI, 133 direction multi shell DWI, and 2 fieldmaps for the functional data (one reversed phase encoding direction, one Siemens deafult fieldmap sequnce) and one fieldmap for the DWI (reversed field encoding direction). An additional reference image of the resting state fMRI is included without multiband factor.

Questionnaires data are also acquired and can be found in the ... fodler.

The proposal can be found here: link

The BIDS conversion was done with heudiconv by the XX project coordinators and/or supported by the Z03 project coordinators.

Defacing
--------------------------------------------------------------------
Defacing was done by the Z03 cooridnator.
Pydeface was used on all anatomical images to ensure deindentification of subjects. The code
can be found at https://github.com/poldracklab/pydeface


Known Issues
--------------------------------------------------------------------
N/A ToDo

--------------------------------------------------------------------


## bids-validator@1.13.1
	[33m1: [WARN] Not all subjects contain the same files. Each subject should contain the same number of files with the same naming unless some files are known to be missing. (code: 38 - INCONSISTENT_SUBJECTS)[39m
		./sub-VP02/anat/sub-VP02_run-02_T1w.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_T1w.json
		./sub-VP02/anat/sub-VP02_run-02_T1w.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_T1w.nii.gz
		./sub-VP02/fmap/sub-VP02_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_acq-bold_dir-PA_run-02_epi.json
		./sub-VP02/fmap/sub-VP02_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP02/fmap/sub-VP02_run-02_magnitude1.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_magnitude1.json
		./sub-VP02/fmap/sub-VP02_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_magnitude1.nii.gz
		./sub-VP02/fmap/sub-VP02_run-02_magnitude2.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_magnitude2.json
		./sub-VP02/fmap/sub-VP02_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_magnitude2.nii.gz
		./sub-VP02/fmap/sub-VP02_run-02_phasediff.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_phasediff.json
		./sub-VP02/fmap/sub-VP02_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_run-02_phasediff.nii.gz
		./sub-VP02/func/sub-VP02_task-rest_run-02_bold.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_task-rest_run-02_bold.json
		./sub-VP02/func/sub-VP02_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_task-rest_run-02_bold.nii.gz
		./sub-VP02/func/sub-VP02_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_task-rest_run-02_sbref.json
		./sub-VP02/func/sub-VP02_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP02, but is present for at least one other subject.
			Evidence: Subject: sub-VP02; Missing file: sub-VP02_task-rest_run-02_sbref.nii.gz
		./sub-VP04/anat/sub-VP04_run-02_T1w.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_T1w.json
		./sub-VP04/anat/sub-VP04_run-02_T1w.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_T1w.nii.gz
		./sub-VP04/fmap/sub-VP04_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_acq-bold_dir-PA_run-02_epi.json
		./sub-VP04/fmap/sub-VP04_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP04/fmap/sub-VP04_run-02_magnitude1.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_magnitude1.json
		./sub-VP04/fmap/sub-VP04_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_magnitude1.nii.gz
		./sub-VP04/fmap/sub-VP04_run-02_magnitude2.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_magnitude2.json
		./sub-VP04/fmap/sub-VP04_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_magnitude2.nii.gz
		./sub-VP04/fmap/sub-VP04_run-02_phasediff.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_phasediff.json
		./sub-VP04/fmap/sub-VP04_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_run-02_phasediff.nii.gz
		./sub-VP04/func/sub-VP04_task-rest_run-02_bold.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_task-rest_run-02_bold.json
		./sub-VP04/func/sub-VP04_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_task-rest_run-02_bold.nii.gz
		./sub-VP04/func/sub-VP04_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_task-rest_run-02_sbref.json
		./sub-VP04/func/sub-VP04_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP04, but is present for at least one other subject.
			Evidence: Subject: sub-VP04; Missing file: sub-VP04_task-rest_run-02_sbref.nii.gz
		./sub-VP06/anat/sub-VP06_run-02_T1w.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_T1w.json
		./sub-VP06/anat/sub-VP06_run-02_T1w.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_T1w.nii.gz
		./sub-VP06/fmap/sub-VP06_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_acq-bold_dir-PA_run-02_epi.json
		./sub-VP06/fmap/sub-VP06_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP06/fmap/sub-VP06_run-02_magnitude1.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_magnitude1.json
		./sub-VP06/fmap/sub-VP06_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_magnitude1.nii.gz
		./sub-VP06/fmap/sub-VP06_run-02_magnitude2.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_magnitude2.json
		./sub-VP06/fmap/sub-VP06_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_magnitude2.nii.gz
		./sub-VP06/fmap/sub-VP06_run-02_phasediff.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_phasediff.json
		./sub-VP06/fmap/sub-VP06_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_run-02_phasediff.nii.gz
		./sub-VP06/func/sub-VP06_task-rest_run-02_bold.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_task-rest_run-02_bold.json
		./sub-VP06/func/sub-VP06_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_task-rest_run-02_bold.nii.gz
		./sub-VP06/func/sub-VP06_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_task-rest_run-02_sbref.json
		./sub-VP06/func/sub-VP06_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP06, but is present for at least one other subject.
			Evidence: Subject: sub-VP06; Missing file: sub-VP06_task-rest_run-02_sbref.nii.gz
		./sub-VP07/anat/sub-VP07_run-02_T1w.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_T1w.json
		./sub-VP07/anat/sub-VP07_run-02_T1w.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_T1w.nii.gz
		./sub-VP07/fmap/sub-VP07_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_acq-bold_dir-PA_run-02_epi.json
		./sub-VP07/fmap/sub-VP07_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP07/fmap/sub-VP07_run-02_magnitude1.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_magnitude1.json
		./sub-VP07/fmap/sub-VP07_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_magnitude1.nii.gz
		./sub-VP07/fmap/sub-VP07_run-02_magnitude2.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_magnitude2.json
		./sub-VP07/fmap/sub-VP07_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_magnitude2.nii.gz
		./sub-VP07/fmap/sub-VP07_run-02_phasediff.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_phasediff.json
		./sub-VP07/fmap/sub-VP07_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_run-02_phasediff.nii.gz
		./sub-VP07/func/sub-VP07_task-rest_run-02_bold.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_task-rest_run-02_bold.json
		./sub-VP07/func/sub-VP07_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_task-rest_run-02_bold.nii.gz
		./sub-VP07/func/sub-VP07_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_task-rest_run-02_sbref.json
		./sub-VP07/func/sub-VP07_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP07, but is present for at least one other subject.
			Evidence: Subject: sub-VP07; Missing file: sub-VP07_task-rest_run-02_sbref.nii.gz
		./sub-VP11/anat/sub-VP11_run-02_T1w.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_T1w.json
		./sub-VP11/anat/sub-VP11_run-02_T1w.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_T1w.nii.gz
		./sub-VP11/fmap/sub-VP11_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_acq-bold_dir-PA_run-02_epi.json
		./sub-VP11/fmap/sub-VP11_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP11/fmap/sub-VP11_run-02_magnitude1.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_magnitude1.json
		./sub-VP11/fmap/sub-VP11_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_magnitude1.nii.gz
		./sub-VP11/fmap/sub-VP11_run-02_magnitude2.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_magnitude2.json
		./sub-VP11/fmap/sub-VP11_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_magnitude2.nii.gz
		./sub-VP11/fmap/sub-VP11_run-02_phasediff.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_phasediff.json
		./sub-VP11/fmap/sub-VP11_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_run-02_phasediff.nii.gz
		./sub-VP11/func/sub-VP11_task-rest_run-02_bold.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_task-rest_run-02_bold.json
		./sub-VP11/func/sub-VP11_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_task-rest_run-02_bold.nii.gz
		./sub-VP11/func/sub-VP11_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_task-rest_run-02_sbref.json
		./sub-VP11/func/sub-VP11_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP11, but is present for at least one other subject.
			Evidence: Subject: sub-VP11; Missing file: sub-VP11_task-rest_run-02_sbref.nii.gz
		./sub-VP14/anat/sub-VP14_run-02_T1w.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_T1w.json
		./sub-VP14/anat/sub-VP14_run-02_T1w.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_T1w.nii.gz
		./sub-VP14/fmap/sub-VP14_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_acq-bold_dir-PA_run-02_epi.json
		./sub-VP14/fmap/sub-VP14_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP14/fmap/sub-VP14_run-02_magnitude1.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_magnitude1.json
		./sub-VP14/fmap/sub-VP14_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_magnitude1.nii.gz
		./sub-VP14/fmap/sub-VP14_run-02_magnitude2.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_magnitude2.json
		./sub-VP14/fmap/sub-VP14_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_magnitude2.nii.gz
		./sub-VP14/fmap/sub-VP14_run-02_phasediff.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_phasediff.json
		./sub-VP14/fmap/sub-VP14_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_run-02_phasediff.nii.gz
		./sub-VP14/func/sub-VP14_task-rest_run-02_bold.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_task-rest_run-02_bold.json
		./sub-VP14/func/sub-VP14_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_task-rest_run-02_bold.nii.gz
		./sub-VP14/func/sub-VP14_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_task-rest_run-02_sbref.json
		./sub-VP14/func/sub-VP14_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP14, but is present for at least one other subject.
			Evidence: Subject: sub-VP14; Missing file: sub-VP14_task-rest_run-02_sbref.nii.gz
		./sub-VP15/anat/sub-VP15_run-02_T1w.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_T1w.json
		./sub-VP15/anat/sub-VP15_run-02_T1w.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_T1w.nii.gz
		./sub-VP15/fmap/sub-VP15_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_acq-bold_dir-PA_run-02_epi.json
		./sub-VP15/fmap/sub-VP15_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP15/fmap/sub-VP15_run-02_magnitude1.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_magnitude1.json
		./sub-VP15/fmap/sub-VP15_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_magnitude1.nii.gz
		./sub-VP15/fmap/sub-VP15_run-02_magnitude2.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_magnitude2.json
		./sub-VP15/fmap/sub-VP15_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_magnitude2.nii.gz
		./sub-VP15/fmap/sub-VP15_run-02_phasediff.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_phasediff.json
		./sub-VP15/fmap/sub-VP15_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_run-02_phasediff.nii.gz
		./sub-VP15/func/sub-VP15_task-rest_run-02_bold.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_task-rest_run-02_bold.json
		./sub-VP15/func/sub-VP15_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_task-rest_run-02_bold.nii.gz
		./sub-VP15/func/sub-VP15_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_task-rest_run-02_sbref.json
		./sub-VP15/func/sub-VP15_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP15, but is present for at least one other subject.
			Evidence: Subject: sub-VP15; Missing file: sub-VP15_task-rest_run-02_sbref.nii.gz
		./sub-VP17/anat/sub-VP17_run-02_T1w.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_T1w.json
		./sub-VP17/anat/sub-VP17_run-02_T1w.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_T1w.nii.gz
		./sub-VP17/fmap/sub-VP17_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_acq-bold_dir-PA_run-02_epi.json
		./sub-VP17/fmap/sub-VP17_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP17/fmap/sub-VP17_run-02_magnitude1.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_magnitude1.json
		./sub-VP17/fmap/sub-VP17_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_magnitude1.nii.gz
		./sub-VP17/fmap/sub-VP17_run-02_magnitude2.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_magnitude2.json
		./sub-VP17/fmap/sub-VP17_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_magnitude2.nii.gz
		./sub-VP17/fmap/sub-VP17_run-02_phasediff.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_phasediff.json
		./sub-VP17/fmap/sub-VP17_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_run-02_phasediff.nii.gz
		./sub-VP17/func/sub-VP17_task-rest_run-02_bold.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_task-rest_run-02_bold.json
		./sub-VP17/func/sub-VP17_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_task-rest_run-02_bold.nii.gz
		./sub-VP17/func/sub-VP17_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_task-rest_run-02_sbref.json
		./sub-VP17/func/sub-VP17_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP17, but is present for at least one other subject.
			Evidence: Subject: sub-VP17; Missing file: sub-VP17_task-rest_run-02_sbref.nii.gz
		./sub-VP18/anat/sub-VP18_run-01_T1w.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_T1w.json
		./sub-VP18/anat/sub-VP18_run-01_T1w.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_T1w.nii.gz
		./sub-VP18/fmap/sub-VP18_acq-bold_dir-PA_run-01_epi.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_acq-bold_dir-PA_run-01_epi.json
		./sub-VP18/fmap/sub-VP18_acq-bold_dir-PA_run-01_epi.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_acq-bold_dir-PA_run-01_epi.nii.gz
		./sub-VP18/fmap/sub-VP18_run-01_magnitude1.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_magnitude1.json
		./sub-VP18/fmap/sub-VP18_run-01_magnitude1.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_magnitude1.nii.gz
		./sub-VP18/fmap/sub-VP18_run-01_magnitude2.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_magnitude2.json
		./sub-VP18/fmap/sub-VP18_run-01_magnitude2.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_magnitude2.nii.gz
		./sub-VP18/fmap/sub-VP18_run-01_phasediff.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_phasediff.json
		./sub-VP18/fmap/sub-VP18_run-01_phasediff.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_run-01_phasediff.nii.gz
		./sub-VP18/func/sub-VP18_task-rest_run-01_bold.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_task-rest_run-01_bold.json
		./sub-VP18/func/sub-VP18_task-rest_run-01_bold.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_task-rest_run-01_bold.nii.gz
		./sub-VP18/func/sub-VP18_task-rest_run-01_sbref.json
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_task-rest_run-01_sbref.json
		./sub-VP18/func/sub-VP18_task-rest_run-01_sbref.nii.gz
			This file is missing for subject sub-VP18, but is present for at least one other subject.
			Evidence: Subject: sub-VP18; Missing file: sub-VP18_task-rest_run-01_sbref.nii.gz
		./sub-VP19/anat/sub-VP19_run-02_T1w.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_T1w.json
		./sub-VP19/anat/sub-VP19_run-02_T1w.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_T1w.nii.gz
		./sub-VP19/fmap/sub-VP19_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_acq-bold_dir-PA_run-02_epi.json
		./sub-VP19/fmap/sub-VP19_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP19/fmap/sub-VP19_run-02_magnitude1.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_magnitude1.json
		./sub-VP19/fmap/sub-VP19_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_magnitude1.nii.gz
		./sub-VP19/fmap/sub-VP19_run-02_magnitude2.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_magnitude2.json
		./sub-VP19/fmap/sub-VP19_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_magnitude2.nii.gz
		./sub-VP19/fmap/sub-VP19_run-02_phasediff.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_phasediff.json
		./sub-VP19/fmap/sub-VP19_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_run-02_phasediff.nii.gz
		./sub-VP19/func/sub-VP19_task-rest_run-02_bold.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_task-rest_run-02_bold.json
		./sub-VP19/func/sub-VP19_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_task-rest_run-02_bold.nii.gz
		./sub-VP19/func/sub-VP19_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_task-rest_run-02_sbref.json
		./sub-VP19/func/sub-VP19_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP19, but is present for at least one other subject.
			Evidence: Subject: sub-VP19; Missing file: sub-VP19_task-rest_run-02_sbref.nii.gz
		./sub-VP20/anat/sub-VP20_run-02_T1w.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_T1w.json
		./sub-VP20/anat/sub-VP20_run-02_T1w.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_T1w.nii.gz
		./sub-VP20/fmap/sub-VP20_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_acq-bold_dir-PA_run-02_epi.json
		./sub-VP20/fmap/sub-VP20_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP20/fmap/sub-VP20_run-02_magnitude1.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_magnitude1.json
		./sub-VP20/fmap/sub-VP20_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_magnitude1.nii.gz
		./sub-VP20/fmap/sub-VP20_run-02_magnitude2.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_magnitude2.json
		./sub-VP20/fmap/sub-VP20_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_magnitude2.nii.gz
		./sub-VP20/fmap/sub-VP20_run-02_phasediff.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_phasediff.json
		./sub-VP20/fmap/sub-VP20_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_run-02_phasediff.nii.gz
		./sub-VP20/func/sub-VP20_task-rest_run-02_bold.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_task-rest_run-02_bold.json
		./sub-VP20/func/sub-VP20_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_task-rest_run-02_bold.nii.gz
		./sub-VP20/func/sub-VP20_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_task-rest_run-02_sbref.json
		./sub-VP20/func/sub-VP20_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP20, but is present for at least one other subject.
			Evidence: Subject: sub-VP20; Missing file: sub-VP20_task-rest_run-02_sbref.nii.gz
		./sub-VP22/anat/sub-VP22_run-02_T1w.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_T1w.json
		./sub-VP22/anat/sub-VP22_run-02_T1w.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_T1w.nii.gz
		./sub-VP22/fmap/sub-VP22_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_acq-bold_dir-PA_run-02_epi.json
		./sub-VP22/fmap/sub-VP22_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP22/fmap/sub-VP22_run-02_magnitude1.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_magnitude1.json
		./sub-VP22/fmap/sub-VP22_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_magnitude1.nii.gz
		./sub-VP22/fmap/sub-VP22_run-02_magnitude2.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_magnitude2.json
		./sub-VP22/fmap/sub-VP22_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_magnitude2.nii.gz
		./sub-VP22/fmap/sub-VP22_run-02_phasediff.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_phasediff.json
		./sub-VP22/fmap/sub-VP22_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_run-02_phasediff.nii.gz
		./sub-VP22/func/sub-VP22_task-rest_run-02_bold.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_task-rest_run-02_bold.json
		./sub-VP22/func/sub-VP22_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_task-rest_run-02_bold.nii.gz
		./sub-VP22/func/sub-VP22_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_task-rest_run-02_sbref.json
		./sub-VP22/func/sub-VP22_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP22, but is present for at least one other subject.
			Evidence: Subject: sub-VP22; Missing file: sub-VP22_task-rest_run-02_sbref.nii.gz
		./sub-VP24/anat/sub-VP24_run-02_T1w.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_T1w.json
		./sub-VP24/anat/sub-VP24_run-02_T1w.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_T1w.nii.gz
		./sub-VP24/fmap/sub-VP24_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_acq-bold_dir-PA_run-02_epi.json
		./sub-VP24/fmap/sub-VP24_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP24/fmap/sub-VP24_run-02_magnitude1.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_magnitude1.json
		./sub-VP24/fmap/sub-VP24_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_magnitude1.nii.gz
		./sub-VP24/fmap/sub-VP24_run-02_magnitude2.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_magnitude2.json
		./sub-VP24/fmap/sub-VP24_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_magnitude2.nii.gz
		./sub-VP24/fmap/sub-VP24_run-02_phasediff.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_phasediff.json
		./sub-VP24/fmap/sub-VP24_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_run-02_phasediff.nii.gz
		./sub-VP24/func/sub-VP24_task-rest_run-02_bold.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_task-rest_run-02_bold.json
		./sub-VP24/func/sub-VP24_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_task-rest_run-02_bold.nii.gz
		./sub-VP24/func/sub-VP24_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_task-rest_run-02_sbref.json
		./sub-VP24/func/sub-VP24_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP24, but is present for at least one other subject.
			Evidence: Subject: sub-VP24; Missing file: sub-VP24_task-rest_run-02_sbref.nii.gz
		./sub-VP28/anat/sub-VP28_run-02_T1w.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_T1w.json
		./sub-VP28/anat/sub-VP28_run-02_T1w.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_T1w.nii.gz
		./sub-VP28/fmap/sub-VP28_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_acq-bold_dir-PA_run-02_epi.json
		./sub-VP28/fmap/sub-VP28_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP28/fmap/sub-VP28_run-02_magnitude1.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_magnitude1.json
		./sub-VP28/fmap/sub-VP28_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_magnitude1.nii.gz
		./sub-VP28/fmap/sub-VP28_run-02_magnitude2.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_magnitude2.json
		./sub-VP28/fmap/sub-VP28_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_magnitude2.nii.gz
		./sub-VP28/fmap/sub-VP28_run-02_phasediff.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_phasediff.json
		./sub-VP28/fmap/sub-VP28_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_run-02_phasediff.nii.gz
		./sub-VP28/func/sub-VP28_task-rest_run-02_bold.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_task-rest_run-02_bold.json
		./sub-VP28/func/sub-VP28_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_task-rest_run-02_bold.nii.gz
		./sub-VP28/func/sub-VP28_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_task-rest_run-02_sbref.json
		./sub-VP28/func/sub-VP28_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP28, but is present for at least one other subject.
			Evidence: Subject: sub-VP28; Missing file: sub-VP28_task-rest_run-02_sbref.nii.gz
		./sub-VP29/anat/sub-VP29_run-02_T1w.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_T1w.json
		./sub-VP29/anat/sub-VP29_run-02_T1w.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_T1w.nii.gz
		./sub-VP29/fmap/sub-VP29_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_acq-bold_dir-PA_run-02_epi.json
		./sub-VP29/fmap/sub-VP29_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP29/fmap/sub-VP29_run-02_magnitude1.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_magnitude1.json
		./sub-VP29/fmap/sub-VP29_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_magnitude1.nii.gz
		./sub-VP29/fmap/sub-VP29_run-02_magnitude2.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_magnitude2.json
		./sub-VP29/fmap/sub-VP29_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_magnitude2.nii.gz
		./sub-VP29/fmap/sub-VP29_run-02_phasediff.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_phasediff.json
		./sub-VP29/fmap/sub-VP29_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_run-02_phasediff.nii.gz
		./sub-VP29/func/sub-VP29_task-rest_run-02_bold.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_task-rest_run-02_bold.json
		./sub-VP29/func/sub-VP29_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_task-rest_run-02_bold.nii.gz
		./sub-VP29/func/sub-VP29_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_task-rest_run-02_sbref.json
		./sub-VP29/func/sub-VP29_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP29, but is present for at least one other subject.
			Evidence: Subject: sub-VP29; Missing file: sub-VP29_task-rest_run-02_sbref.nii.gz
		./sub-VP31/anat/sub-VP31_run-02_T1w.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_T1w.json
		./sub-VP31/anat/sub-VP31_run-02_T1w.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_T1w.nii.gz
		./sub-VP31/fmap/sub-VP31_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_acq-bold_dir-PA_run-02_epi.json
		./sub-VP31/fmap/sub-VP31_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP31/fmap/sub-VP31_run-02_magnitude1.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_magnitude1.json
		./sub-VP31/fmap/sub-VP31_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_magnitude1.nii.gz
		./sub-VP31/fmap/sub-VP31_run-02_magnitude2.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_magnitude2.json
		./sub-VP31/fmap/sub-VP31_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_magnitude2.nii.gz
		./sub-VP31/fmap/sub-VP31_run-02_phasediff.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_phasediff.json
		./sub-VP31/fmap/sub-VP31_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_run-02_phasediff.nii.gz
		./sub-VP31/func/sub-VP31_task-rest_run-02_bold.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_task-rest_run-02_bold.json
		./sub-VP31/func/sub-VP31_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_task-rest_run-02_bold.nii.gz
		./sub-VP31/func/sub-VP31_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_task-rest_run-02_sbref.json
		./sub-VP31/func/sub-VP31_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP31, but is present for at least one other subject.
			Evidence: Subject: sub-VP31; Missing file: sub-VP31_task-rest_run-02_sbref.nii.gz
		./sub-VP35/anat/sub-VP35_run-02_T1w.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_T1w.json
		./sub-VP35/anat/sub-VP35_run-02_T1w.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_T1w.nii.gz
		./sub-VP35/fmap/sub-VP35_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_acq-bold_dir-PA_run-02_epi.json
		./sub-VP35/fmap/sub-VP35_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP35/fmap/sub-VP35_run-02_magnitude1.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_magnitude1.json
		./sub-VP35/fmap/sub-VP35_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_magnitude1.nii.gz
		./sub-VP35/fmap/sub-VP35_run-02_magnitude2.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_magnitude2.json
		./sub-VP35/fmap/sub-VP35_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_magnitude2.nii.gz
		./sub-VP35/fmap/sub-VP35_run-02_phasediff.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_phasediff.json
		./sub-VP35/fmap/sub-VP35_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_run-02_phasediff.nii.gz
		./sub-VP35/func/sub-VP35_task-rest_run-02_bold.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_task-rest_run-02_bold.json
		./sub-VP35/func/sub-VP35_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_task-rest_run-02_bold.nii.gz
		./sub-VP35/func/sub-VP35_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_task-rest_run-02_sbref.json
		./sub-VP35/func/sub-VP35_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP35, but is present for at least one other subject.
			Evidence: Subject: sub-VP35; Missing file: sub-VP35_task-rest_run-02_sbref.nii.gz
		./sub-VP41/anat/sub-VP41_run-02_T1w.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_T1w.json
		./sub-VP41/anat/sub-VP41_run-02_T1w.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_T1w.nii.gz
		./sub-VP41/fmap/sub-VP41_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_acq-bold_dir-PA_run-02_epi.json
		./sub-VP41/fmap/sub-VP41_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP41/fmap/sub-VP41_run-02_magnitude1.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_magnitude1.json
		./sub-VP41/fmap/sub-VP41_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_magnitude1.nii.gz
		./sub-VP41/fmap/sub-VP41_run-02_magnitude2.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_magnitude2.json
		./sub-VP41/fmap/sub-VP41_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_magnitude2.nii.gz
		./sub-VP41/fmap/sub-VP41_run-02_phasediff.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_phasediff.json
		./sub-VP41/fmap/sub-VP41_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_run-02_phasediff.nii.gz
		./sub-VP41/func/sub-VP41_task-rest_run-02_bold.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_task-rest_run-02_bold.json
		./sub-VP41/func/sub-VP41_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_task-rest_run-02_bold.nii.gz
		./sub-VP41/func/sub-VP41_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_task-rest_run-02_sbref.json
		./sub-VP41/func/sub-VP41_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP41, but is present for at least one other subject.
			Evidence: Subject: sub-VP41; Missing file: sub-VP41_task-rest_run-02_sbref.nii.gz
		./sub-VP42/anat/sub-VP42_run-02_T1w.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_T1w.json
		./sub-VP42/anat/sub-VP42_run-02_T1w.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_T1w.nii.gz
		./sub-VP42/fmap/sub-VP42_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_acq-bold_dir-PA_run-02_epi.json
		./sub-VP42/fmap/sub-VP42_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP42/fmap/sub-VP42_run-02_magnitude1.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_magnitude1.json
		./sub-VP42/fmap/sub-VP42_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_magnitude1.nii.gz
		./sub-VP42/fmap/sub-VP42_run-02_magnitude2.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_magnitude2.json
		./sub-VP42/fmap/sub-VP42_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_magnitude2.nii.gz
		./sub-VP42/fmap/sub-VP42_run-02_phasediff.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_phasediff.json
		./sub-VP42/fmap/sub-VP42_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_run-02_phasediff.nii.gz
		./sub-VP42/func/sub-VP42_task-rest_run-02_bold.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_task-rest_run-02_bold.json
		./sub-VP42/func/sub-VP42_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_task-rest_run-02_bold.nii.gz
		./sub-VP42/func/sub-VP42_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_task-rest_run-02_sbref.json
		./sub-VP42/func/sub-VP42_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP42, but is present for at least one other subject.
			Evidence: Subject: sub-VP42; Missing file: sub-VP42_task-rest_run-02_sbref.nii.gz
		./sub-VP43/anat/sub-VP43_run-02_T1w.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_T1w.json
		./sub-VP43/anat/sub-VP43_run-02_T1w.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_T1w.nii.gz
		./sub-VP43/fmap/sub-VP43_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_acq-bold_dir-PA_run-02_epi.json
		./sub-VP43/fmap/sub-VP43_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP43/fmap/sub-VP43_run-02_magnitude1.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_magnitude1.json
		./sub-VP43/fmap/sub-VP43_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_magnitude1.nii.gz
		./sub-VP43/fmap/sub-VP43_run-02_magnitude2.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_magnitude2.json
		./sub-VP43/fmap/sub-VP43_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_magnitude2.nii.gz
		./sub-VP43/fmap/sub-VP43_run-02_phasediff.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_phasediff.json
		./sub-VP43/fmap/sub-VP43_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_run-02_phasediff.nii.gz
		./sub-VP43/func/sub-VP43_task-rest_run-02_bold.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_task-rest_run-02_bold.json
		./sub-VP43/func/sub-VP43_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_task-rest_run-02_bold.nii.gz
		./sub-VP43/func/sub-VP43_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_task-rest_run-02_sbref.json
		./sub-VP43/func/sub-VP43_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP43, but is present for at least one other subject.
			Evidence: Subject: sub-VP43; Missing file: sub-VP43_task-rest_run-02_sbref.nii.gz
		./sub-VP44/anat/sub-VP44_run-02_T1w.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_T1w.json
		./sub-VP44/anat/sub-VP44_run-02_T1w.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_T1w.nii.gz
		./sub-VP44/fmap/sub-VP44_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_acq-bold_dir-PA_run-02_epi.json
		./sub-VP44/fmap/sub-VP44_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP44/fmap/sub-VP44_run-02_magnitude1.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_magnitude1.json
		./sub-VP44/fmap/sub-VP44_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_magnitude1.nii.gz
		./sub-VP44/fmap/sub-VP44_run-02_magnitude2.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_magnitude2.json
		./sub-VP44/fmap/sub-VP44_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_magnitude2.nii.gz
		./sub-VP44/fmap/sub-VP44_run-02_phasediff.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_phasediff.json
		./sub-VP44/fmap/sub-VP44_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_run-02_phasediff.nii.gz
		./sub-VP44/func/sub-VP44_task-rest_run-02_bold.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_task-rest_run-02_bold.json
		./sub-VP44/func/sub-VP44_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_task-rest_run-02_bold.nii.gz
		./sub-VP44/func/sub-VP44_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_task-rest_run-02_sbref.json
		./sub-VP44/func/sub-VP44_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP44, but is present for at least one other subject.
			Evidence: Subject: sub-VP44; Missing file: sub-VP44_task-rest_run-02_sbref.nii.gz
		./sub-VP46/anat/sub-VP46_run-02_T1w.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_T1w.json
		./sub-VP46/anat/sub-VP46_run-02_T1w.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_T1w.nii.gz
		./sub-VP46/fmap/sub-VP46_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_acq-bold_dir-PA_run-02_epi.json
		./sub-VP46/fmap/sub-VP46_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP46/fmap/sub-VP46_run-02_magnitude1.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_magnitude1.json
		./sub-VP46/fmap/sub-VP46_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_magnitude1.nii.gz
		./sub-VP46/fmap/sub-VP46_run-02_magnitude2.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_magnitude2.json
		./sub-VP46/fmap/sub-VP46_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_magnitude2.nii.gz
		./sub-VP46/fmap/sub-VP46_run-02_phasediff.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_phasediff.json
		./sub-VP46/fmap/sub-VP46_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_run-02_phasediff.nii.gz
		./sub-VP46/func/sub-VP46_task-rest_run-02_bold.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_task-rest_run-02_bold.json
		./sub-VP46/func/sub-VP46_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_task-rest_run-02_bold.nii.gz
		./sub-VP46/func/sub-VP46_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_task-rest_run-02_sbref.json
		./sub-VP46/func/sub-VP46_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP46, but is present for at least one other subject.
			Evidence: Subject: sub-VP46; Missing file: sub-VP46_task-rest_run-02_sbref.nii.gz
		./sub-VP48/anat/sub-VP48_run-02_T1w.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_T1w.json
		./sub-VP48/anat/sub-VP48_run-02_T1w.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_T1w.nii.gz
		./sub-VP48/fmap/sub-VP48_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_acq-bold_dir-PA_run-02_epi.json
		./sub-VP48/fmap/sub-VP48_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP48/fmap/sub-VP48_run-02_magnitude1.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_magnitude1.json
		./sub-VP48/fmap/sub-VP48_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_magnitude1.nii.gz
		./sub-VP48/fmap/sub-VP48_run-02_magnitude2.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_magnitude2.json
		./sub-VP48/fmap/sub-VP48_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_magnitude2.nii.gz
		./sub-VP48/fmap/sub-VP48_run-02_phasediff.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_phasediff.json
		./sub-VP48/fmap/sub-VP48_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_run-02_phasediff.nii.gz
		./sub-VP48/func/sub-VP48_task-rest_run-02_bold.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_task-rest_run-02_bold.json
		./sub-VP48/func/sub-VP48_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_task-rest_run-02_bold.nii.gz
		./sub-VP48/func/sub-VP48_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_task-rest_run-02_sbref.json
		./sub-VP48/func/sub-VP48_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP48, but is present for at least one other subject.
			Evidence: Subject: sub-VP48; Missing file: sub-VP48_task-rest_run-02_sbref.nii.gz
		./sub-VP50/anat/sub-VP50_run-02_T1w.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_T1w.json
		./sub-VP50/anat/sub-VP50_run-02_T1w.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_T1w.nii.gz
		./sub-VP50/fmap/sub-VP50_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_acq-bold_dir-PA_run-02_epi.json
		./sub-VP50/fmap/sub-VP50_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP50/fmap/sub-VP50_run-02_magnitude1.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_magnitude1.json
		./sub-VP50/fmap/sub-VP50_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_magnitude1.nii.gz
		./sub-VP50/fmap/sub-VP50_run-02_magnitude2.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_magnitude2.json
		./sub-VP50/fmap/sub-VP50_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_magnitude2.nii.gz
		./sub-VP50/fmap/sub-VP50_run-02_phasediff.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_phasediff.json
		./sub-VP50/fmap/sub-VP50_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_run-02_phasediff.nii.gz
		./sub-VP50/func/sub-VP50_task-rest_run-02_bold.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_task-rest_run-02_bold.json
		./sub-VP50/func/sub-VP50_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_task-rest_run-02_bold.nii.gz
		./sub-VP50/func/sub-VP50_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_task-rest_run-02_sbref.json
		./sub-VP50/func/sub-VP50_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP50, but is present for at least one other subject.
			Evidence: Subject: sub-VP50; Missing file: sub-VP50_task-rest_run-02_sbref.nii.gz
		./sub-VP51/anat/sub-VP51_run-02_T1w.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_T1w.json
		./sub-VP51/anat/sub-VP51_run-02_T1w.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_T1w.nii.gz
		./sub-VP51/fmap/sub-VP51_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_acq-bold_dir-PA_run-02_epi.json
		./sub-VP51/fmap/sub-VP51_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP51/fmap/sub-VP51_run-02_magnitude1.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_magnitude1.json
		./sub-VP51/fmap/sub-VP51_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_magnitude1.nii.gz
		./sub-VP51/fmap/sub-VP51_run-02_magnitude2.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_magnitude2.json
		./sub-VP51/fmap/sub-VP51_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_magnitude2.nii.gz
		./sub-VP51/fmap/sub-VP51_run-02_phasediff.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_phasediff.json
		./sub-VP51/fmap/sub-VP51_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_run-02_phasediff.nii.gz
		./sub-VP51/func/sub-VP51_task-rest_run-02_bold.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_task-rest_run-02_bold.json
		./sub-VP51/func/sub-VP51_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_task-rest_run-02_bold.nii.gz
		./sub-VP51/func/sub-VP51_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_task-rest_run-02_sbref.json
		./sub-VP51/func/sub-VP51_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP51, but is present for at least one other subject.
			Evidence: Subject: sub-VP51; Missing file: sub-VP51_task-rest_run-02_sbref.nii.gz
		./sub-VP52/anat/sub-VP52_run-02_T1w.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_T1w.json
		./sub-VP52/anat/sub-VP52_run-02_T1w.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_T1w.nii.gz
		./sub-VP52/fmap/sub-VP52_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_acq-bold_dir-PA_run-02_epi.json
		./sub-VP52/fmap/sub-VP52_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP52/fmap/sub-VP52_run-02_magnitude1.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_magnitude1.json
		./sub-VP52/fmap/sub-VP52_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_magnitude1.nii.gz
		./sub-VP52/fmap/sub-VP52_run-02_magnitude2.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_magnitude2.json
		./sub-VP52/fmap/sub-VP52_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_magnitude2.nii.gz
		./sub-VP52/fmap/sub-VP52_run-02_phasediff.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_phasediff.json
		./sub-VP52/fmap/sub-VP52_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_run-02_phasediff.nii.gz
		./sub-VP52/func/sub-VP52_task-rest_run-02_bold.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_task-rest_run-02_bold.json
		./sub-VP52/func/sub-VP52_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_task-rest_run-02_bold.nii.gz
		./sub-VP52/func/sub-VP52_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_task-rest_run-02_sbref.json
		./sub-VP52/func/sub-VP52_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP52, but is present for at least one other subject.
			Evidence: Subject: sub-VP52; Missing file: sub-VP52_task-rest_run-02_sbref.nii.gz
		./sub-VP58/anat/sub-VP58_run-02_T1w.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_T1w.json
		./sub-VP58/anat/sub-VP58_run-02_T1w.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_T1w.nii.gz
		./sub-VP58/fmap/sub-VP58_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_acq-bold_dir-PA_run-02_epi.json
		./sub-VP58/fmap/sub-VP58_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP58/fmap/sub-VP58_run-02_magnitude1.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_magnitude1.json
		./sub-VP58/fmap/sub-VP58_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_magnitude1.nii.gz
		./sub-VP58/fmap/sub-VP58_run-02_magnitude2.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_magnitude2.json
		./sub-VP58/fmap/sub-VP58_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_magnitude2.nii.gz
		./sub-VP58/fmap/sub-VP58_run-02_phasediff.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_phasediff.json
		./sub-VP58/fmap/sub-VP58_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_run-02_phasediff.nii.gz
		./sub-VP58/func/sub-VP58_task-rest_run-02_bold.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_task-rest_run-02_bold.json
		./sub-VP58/func/sub-VP58_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_task-rest_run-02_bold.nii.gz
		./sub-VP58/func/sub-VP58_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_task-rest_run-02_sbref.json
		./sub-VP58/func/sub-VP58_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP58, but is present for at least one other subject.
			Evidence: Subject: sub-VP58; Missing file: sub-VP58_task-rest_run-02_sbref.nii.gz
		./sub-VP59/anat/sub-VP59_run-02_T1w.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_T1w.json
		./sub-VP59/anat/sub-VP59_run-02_T1w.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_T1w.nii.gz
		./sub-VP59/fmap/sub-VP59_acq-bold_dir-PA_run-02_epi.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_acq-bold_dir-PA_run-02_epi.json
		./sub-VP59/fmap/sub-VP59_acq-bold_dir-PA_run-02_epi.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_acq-bold_dir-PA_run-02_epi.nii.gz
		./sub-VP59/fmap/sub-VP59_run-02_magnitude1.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_magnitude1.json
		./sub-VP59/fmap/sub-VP59_run-02_magnitude1.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_magnitude1.nii.gz
		./sub-VP59/fmap/sub-VP59_run-02_magnitude2.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_magnitude2.json
		./sub-VP59/fmap/sub-VP59_run-02_magnitude2.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_magnitude2.nii.gz
		./sub-VP59/fmap/sub-VP59_run-02_phasediff.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_phasediff.json
		./sub-VP59/fmap/sub-VP59_run-02_phasediff.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_run-02_phasediff.nii.gz
		./sub-VP59/func/sub-VP59_task-rest_run-02_bold.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_task-rest_run-02_bold.json
		./sub-VP59/func/sub-VP59_task-rest_run-02_bold.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_task-rest_run-02_bold.nii.gz
		./sub-VP59/func/sub-VP59_task-rest_run-02_sbref.json
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_task-rest_run-02_sbref.json
		./sub-VP59/func/sub-VP59_task-rest_run-02_sbref.nii.gz
			This file is missing for subject sub-VP59, but is present for at least one other subject.
			Evidence: Subject: sub-VP59; Missing file: sub-VP59_task-rest_run-02_sbref.nii.gz

[36m	Please visit https://neurostars.org/search?q=INCONSISTENT_SUBJECTS for existing conversations about this issue.[39m

        [34m[4mSummary:[24m[39m                [34m[4mAvailable Tasks:[24m[39m                     [34m[4mAvailable Modalities:[39m[24m 
        595 Files, 7.1GB        rest                                 MRI                   
        28 - Subjects           TODO: full task name for rest                              
        1 - Session                                                                        


[36m	If you have any questions, please post on https://neurostars.org/tags/bids.[39m
