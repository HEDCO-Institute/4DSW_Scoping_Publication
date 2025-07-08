
# **Replication Package for 2025 Educational Evaluation and Policy Analysis Publication**
<!-- TODO: UPDATE WITH JOURNAL NAME AND DATE AFTER PUBLICATION--->

**Date of Release:** 4/16/2025  
**Title:** The Four-Day School Week at K-12 Schools in the United States: A Scoping Review of Empirical Research Evidence <br>
**OSF Component:** <https://osf.io/5rgps/> <br> 
**Package Author:** Shaina Trevino 



## **🔹 Overview**
This folder contains the replication materials for the following publication:  

<!-- TODO: INSERT CITATION/DOI AFTER PUBLICATION -->
Grant, S., Trevino, S. D., Steinka-Fry, K., Day, E., Cabrera, B., Hamilton, S., Martinez, S., Chinn, L. K., & Tanner-Smith, E. E. (Under Review). The four-day school week at K-12 schools in the United States: A scoping review of empirical research evidence.

This replication package follows **[AEA Data and Code Availability Standards](https://datacodestandard.org/)** and includes:
- Datasets used to generate reported results.
- R code necessary to reproduce quantitative results reported.
- Computational environment details to ensure reproducibility.


## **🔹 Data and Code Availability Statement**
### **Data Sources**
The data used in this publication include review and study characteristics from our larger [living scoping review on the four-day school week](https://github.com/HEDCO-Institute/4DSW_Scoping_Review)
- Datasets from the living review used for this publication reflect a fixed version of the data, captured during analysis. 
- A data dictionary, including variable-level information for all data files, is provided in the `data` subfolder (`data_dictionary.xlsx`).

The following datasets used for analyses are available in the `data` subfolder:

| Data File | Description | Data Structure |
|-----------|-------------|-----------| 
| `4dsw_all_citations.xlsx` | APA reference citation for all records screened | One row per citation | 
| `4dsw_eligibility_data.xlsx` | Screening and eligibility decisions | One row per citation |
| `4dsw_linked_references.xlsx` | Citation information for additional reports of studies | One row per main study + report combination |
| `4dsw_study_data.xlsx` | Extracted descriptive data for eligible primary studies | One row per eligible primary study | 
| `data_dictionary.xlsx` | Variable information for each data file (in separate tabs) | One row per variable | 
<br>

### **Analysis Script**
The analysis script used to generate quantitative results for this publication is an `Rmarkdown` file in the `code` subfolder (`2025_EEPA_Analysis_Script.Rmd`). 

### **Data Citation**
Please cite this version of the data as follows:

<!-- TODO: INSERT CITATION/DOI AFTER PUBLICATION -->
Trevino, S. D., Grant, S., Steinka-Fry, K., Day, E., Cabrera, B., Hamilton, S., Martinez, S., Chinn, L. K., & Tanner-Smith, E. E. (2025). Data for "The four-day school week at K-12 schools in the United States: A scoping review of empirical research evidence". [OSF](https://osf.io/5rgps/). https://doi.org/10.17605/OSF.IO/5RGPS

### **Handling of Missing Data**
- Missing values in the datasets are coded as `-999`, `Not Reported`, or `NA` and indicate those values were not reported in studies/reviews.


## **🔹 Instructions for Replication**

### **Data Preparation and Analysis**
To replicate our results: 

**If you have Rstudio and Git installed and connected to your GitHub account:**

1. Clone the [repository](https://github.com/HEDCO-Institute/4DSW_Scoping_Publication) to your local machine ([click for help](https://book.cds101.com/using-rstudio-server-to-clone-a-github-repo-as-a-new-project.html#step---2))
1. Open the `4DSW_Scoping_Publication.Rproj` R project in R Studio (this should automatically activate the `renv` environment)
1. Navigate to the `code` folder
1. Run the `2025_EEPA_Analysis_Script.Rmd` script 

**If you need to install or connect R, Rstudio, Git, and/or GitHub:**

1. [Create a GitHub account](https://happygitwithr.com/github-acct.html#github-acct)
1. [Install R and RStudio](https://happygitwithr.com/install-r-rstudio.html)
1. [Install Git](https://happygitwithr.com/install-git.html)
1. [Link Git to your GitHub account](https://happygitwithr.com/hello-git.html)
1. [Sign into GitHub in Rstudio](https://happygitwithr.com/https-pat.html)

**To reproduce our results without using Git and GitHub, you may use the following steps:** 

1. Download the ZIP file from the [repository](https://github.com/HEDCO-Institute/4DSW_Scoping_Publication)
1. Extract all files to your local machine
1. Open the `4DSW_Scoping_Publication.Rproj` R project in R Studio (this will automatically set the working directory and activate the `renv` environment)
1. Navigate to the `code` folder
1. Run the `2025_EEPA_Analysis_Script.Rmd` script 


## **🔹 Notes on Reproducibility**
- The `renv` environment should be loaded automatically, but the `.Rmd` contains code to restore the environment if needed (`renv::restore()`)
- All file paths are relative to the R project; no hardcoded paths are used.
- Data cleaning and analyses are fully automated in the provided `.Rmd` analysis script.

### **Non-Reproducible Elements**
Some components cannot be reproduced using the analysis script:
- Qualitative findings, such as the specific themes, are not generated by the analysis script. 
- Figure 1 was manually created in Word but those numbers are still generated in the analysis script.
- Supplement 1 was manually created in Word and is not generated by the analysis script. 

### **Known Discrepancies**
<!-- TODO: INSERT CITATION/DOI AFTER PUBLICATION -->
The following discrepancies were identified after publication through an external computational reproducibility check: 
- The numbers reported for community type are slightly off. The manuscript erroneously states there were 32 suburban and 34 urban communities represented. In the data, there are only 31 suburban and 33 urban communities among included studies. 


## **🔹 Computational Requirements**
### **Software Environment**
- **R Version:** 4.2.2  
- **Operating System:** Windows 10 Enterprise (x86_64-w64-mingw32/x64)  

### **Reproducing the Environment**
Opening the `4DSW_Scoping_Publication` R project should automatically install the correct package versions and set up the environment using the `renv` package. To manually load the environment:

1. Install `renv` (if not already installed):
```r
if (!requireNamespace("renv", quietly = TRUE)) install.packages("renv")
```

2. Restore any missing packages:
```r
renv::restore()
```

3. If needed, load the environment:
```r
renv::load()
```

## **🔹 Folder Structure**
```
📁 4DSW_Scoping_Publication/
│── 📁 code/                   # Analysis scripts for reproducibility
│    └── 2025_EEPA_Analysis_Script.Rmd
│
│── 📁 data/                   # Datasets and dictionary used for this publication
│    ├── 4dsw_all_citations.xlsx
│    ├── 4dsw_eligiblity_data.xlsx
│    ├── 4dsw_linked_references.xlsx
│    ├── 4dsw_study_data.xlsx
│    ├── data_dictionary.xlsx
│
│── 📁 renv/                   # Renv environment for reproducibility
│── 📄 renv.lock               # Package versions and dependencies
│── 📄 .Rprofile               # Renv configuration file
│── 📄 README.md               # This README document
│── 📄 LICENSE                 # Liscense for this repo
```


## **🔹 Licensing**
The code and data in this replication package are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0); see the LICENSE file in the main root directory for full terms



## **🔹 Contact Information**
For questions about this replication package, contact:  
✉️ **Shaina Trevino** (strevino@uoregon.edu)  

