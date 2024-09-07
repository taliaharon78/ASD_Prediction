---

# Notebook:

ASD Prediction (1).ipynb

---

# Goals

The goal of the full research is to assist in early diagnosis of ASD (Autism Spectrum Disorder).  
Early diagnosis is crucial to ASD treatment (bearing in mind the high neuroplasticity at younger ages).  
As babies can have harmless MRI scans (while asleep), prediction of ASD from MRI data would be better suited for early diagnosis than the diagnosis made nowadays from many different kinds of tests done at later ages (tests which I’ll describe shortly in the Data section).  
In the current project, my goal is to predict ASD from the phenotypic data.  
I wish to evaluate the accuracy one can get by using only this data (in order to compare it to the prediction scores we will get from the MRI scans later in our research).

I propose the following framework:

1. **Exploratory Data Analysis (EDA):**  
   ABIDE II is the largest and most global dataset for ASD research. It includes 1,152 subjects (about half of them with ASD).  
   It contains sMRI data, rs-fMRI data, and phenotypic data.  
   In this project, I would like to explore the phenotypic data files, which contain a large set of test scores used by psychiatrists, psychologists, pediatricians, etc., to diagnose ASD.

2. **Feature Selection and Classification:**  
   I will go over the large amount of features in the phenotypic data files and select, using several different methods, only the ones that will help me achieve the best scores on the classification models I intend to apply.  
   I will train classification models and try to predict for each record if the subject has ASD or not.

3. **Dimensionality Reduction and Clustering:**  
   As an alternative to supervised classification models, I will investigate whether I can get better results by applying some "brute force" on the same data using only PCA (Principal Component Analysis) and clustering.


---

# Data

The data related to the subjects in the ABIDE II dataset is split into several files.  
I downloaded them from: [this link](https://www.nitrc.org/frs/downloadlink.php/9108)

The files are grouped as follows:

### Phenotypic data
- **ABIDEII_Composite_Phenotypic:** My main data source for subject classification, containing 1,114 subjects.
- **ABIDEII_Long_Composite_Phenotypic:** Includes data related to an additional 38 subjects. All subjects were scanned twice a few years apart (baseline + follow-up scans). I added all baseline phenotypic data of these 38 subjects to the 1,114 subjects from the first file (resulting in 1,152 subjects for my analysis).
- **ABIDEII_Data_Legend:** Shows for each feature its label, type, description, and range of values.

### MRI related data files:
Will not be used in the scope of this project.

The phenotypic data includes tests for ASD diagnosis alongside tests from other domains with some relevance to ASD.  
To gain more domain knowledge, I discussed the relevance of each test with a child psychologist specializing in ASD diagnosis.  
I also read several articles discussing the different tests.  
A full description of each feature/test, its relevance to ASD, and supporting links can be found in this Google Drive link under **ABIDEII_Data_Legend.xlsx**.
