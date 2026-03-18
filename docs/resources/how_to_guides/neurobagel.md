# ENIGMA‑PD Data Annotation Workflow  
All you need to know about using the Neurobagel Annotation Tool

## Why this matters  
As ENIGMA‑PD moves toward sharing richer clinical, cognitive, and neuropsychiatric data across sites, we need a consistent and reliable way to interpret variables. Manual data dictionaries in spreadsheets are prone to typos, inconsistent naming, and misunderstandings about what each variable represents.  
The Neurobagel workflow provides a structured, user‑friendly way to standardize how we describe clinical data, making it easier to reuse datasets, combine them across sites, and support ENIGMA-PD projects with more advanced clinical measures.

In the future, we hope that the standardized annotations will make it easier for ENIGMA-PD to discover data availability across sites for ongoing and new projects.
You can see a pilot project for this at [enigma.neurobagel.org](https://enigma.neurobagel.org/).

---

## 1. ENIGMA‑PD Custom Variable List  
To support harmonized annotation, ENIGMA‑PD created a curated list of PD‑relevant variables. Standard vocabularies in Neurobagel are broad, and many PD‑specific assessments (cognition, motor, neuropsychiatry, behaviour) were missing.  
The ENIGMA‑PD list fills this gap and ensures that all sites annotate their data using the same shared terminology.

This list is a work in progress and will continue to evolve. We are keen to hear from sites if important variables they collect are missing, so we can expand and refine the list together. Please reach out to enigma-pd@amsterdamumc.nl.

### What this step provides
- A consortium‑wide reference list of PD‑specific assessments and clinical variables.  
- A controlled vocabulary that appears directly inside the Neurobagel Annotation Tool.  
- A mechanism for sites to suggest missing variables.

**Check out the ENIGMA‑PD variable list [here](https://docs.google.com/spreadsheets/d/1pwi6df8LKc3xFENH9JcOUk1HKHARspt-2lUhsy2JYAE/edit?usp=sharing)**  

---

## 2. Annotation using the Neurobagel Tool  
With the ENIGMA‑PD list integrated into the tool, sites can annotate their datasets in a structured and intuitive way.

### What sites do in this step
- Go to [https://beta-annotate.neurobagel.org/](https://beta-annotate.neurobagel.org/)
- Select **ENIGMA-PD** as configuration.

![Neurobagel ENIGMA-PD Configuration](docs/assets/figures/Neurobagel_ENIGMA-PD_Configuration.png)

- Upload a TSV file containing demographic and clinical variables.
- New to Neurobagel? Click through the introduction windows to get started.
- **Column annotation**: Assign each column or group of columns to a standardized variable by clicking on them.
  -  Select multiple related columns at once using CTRL+click or SHIFT+click
  - Can't find a column? Filter your column list by name using the search bar at the top left
  - Can't find a variable? Use the search bar in the assessment tool list to narrow down options
  - If no variable fits your column, please use the *description* field to provide us with more context to understand this column
- **Value annotation**: Review all columns annotated in the previous step and describe their values.
  - Mark missing values.  
  - Optionally add short human‑readable descriptions for uncommon variables.  
- Done? Upload the data dictionary to a protected ENIGMA-PD google drive folder or download it locally and share it with the ENIGMA-PD team by email.

!!! info "Privacy note"
      Although the annotation interface is a web app, it runs entirely on your computer and Neurobagel **does not upload any data or retain data**. Your data are used only to populate the annotation interface (read columns and possible values).

### Why this helps
- Produces a consistent, machine‑readable data dictionary for each cohort.  
- Reduces human error compared to manual data dictionaries. 
(If you make a mistake during annotation, you can simply load your data dictionary into the tool again and correct it)
- Makes datasets easier to understand, reuse, and combine.  

**Check out the Neurobagel documentation [here](https://neurobagel.org/user_guide/annotation_tool/)**  

---

## Feedback from early adopters  
- Annotation is straightforward and user‑friendly. It typically takes under an hour for a dataset of around 100 variables. And if you cannot finish in one go, you can always save your progress and continue later   
- The main time investment is **the column annotation step**, selecting the correct variable from the ENIGMA‑PD list.  
- Overall experience: not difficult, but requires some attention to detail.

??? info "Add your feedback to improve the tool"
    The Neurobagel team continues to improve this tool together with us. If you have an idea for an improvement or find something difficult or confusing, please use the purple button "Give us feedback" on the right edge of the screen

---

## Next steps for sites  
- Annotate your clinical dataset using the ENIGMA‑PD list and Neurobagel tool.  
- Reach out to enigma-pd@amsterdamumc.nl for support!
- Share feedback on missing variables or usability improvements.
