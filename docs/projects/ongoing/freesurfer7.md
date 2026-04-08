# Welcome to the ENIGMA-PD FreeSurfer 7 guidelines!

> **Page update · 8 April 2026** · *You may notice this page looks a bit different. Shared processing instructions are now maintained centrally on the [ENIGMA-infra page](https://enigma-infra.github.io/) to keep all working groups in sync. Where you previously found full step-by-step instructions, you will now find a link to that central page, with any working group-specific notes listed below.*

## On this page
This page is created to guide collaborating ENIGMA-PD sites through the FreeSurfer processing steps. The outcomes include cortical thickness, cortical surface area, and volume of subcortical regions and their subfields. All steps and code required are combined into the guidelines presented here. If you have any questions, concerns, or issues, please contact the ENIGMA-PD core team at enigma-pd@amsterdamumc.nl. 

## Leaderboard
To help motivate and monitor each site's progress, we maintain a leaderboard that outlines all the steps detailed in these guidelines. If you are in charge of data processing at your site, please request access and regularly update your progress on the current steps on the [ENIGMA-PD Leaderboard](https://docs.google.com/spreadsheets/d/13iGfh-97ZYnAyjT5egBDHmGhqXbsl1yo1A6QnPXQYbY/edit?usp=sharing).

## Overview
The figure shows the expected outcomes and corresponding processing steps - most of which can be performed using the Nipoppy framework and helper Python package. We strongly recommend adoption of Nipoppy tools to simplify coordination and ensure reproducibility of this end-to-end process across all sites. 
![enigma-nipoppy-FS7-upgrade-overview](https://github.com/user-attachments/assets/aae8449c-58cf-4889-92de-979f79082e28)

## Setting up Nipoppy: [Link to instructions](https://enigma-infra.github.io/resources/how_to_guides/setting_up_nipoppy/){:target="_blank"}
Nipoppy is a lightweight framework for standardized data organization and processing of neuroimaging-clinical datasets. Its goal is to help users adopt the [FAIR principles](https://www.go-fair.org/fair-principles/){:target="_blank"} and improve the reproducibility of studies. 

The ongoing collaboration between the ENIGMA-PD team and Nipoppy team has streamlined data curation, processing, and analysis workflows, which significantly simplifies tracking of data availability, addition of new pipelines and upgrading of existing pipelines. The ENIGMA-Tremor and Nipoppy team is available to support and guide users through the process of implementing the framework, ensuring a smooth transition. To join the Nipoppy support community, we recommend joining their [Discord channel](https://discord.gg/dQGYADCCMB){:target="_blank"}. Here you can ask questions and find answers while working with Nipoppy. 

For more information, see the [Nipoppy documentation](https://nipoppy.readthedocs.io/en/stable/index.html){:target="_blank"}.

**Here, primairly we will use Nipoppy to help you with 1) BIDSification, 2) FreeSurfer7 processing, 3) Sub-segmentation and 4) Quality control.** 

## Running FreeSurfer 7
When you reach this point, the hardest part is behind you and we can finally come to the real stuff. We will run FreeSurfer 7 through fMRIPrep using Nipoppy. See [here](https://nipoppy.readthedocs.io/en/latest/how_to_guides/pipeline_run/index.html) for additional information about running processing pipelines with Nipoppy.

### Cortical and subcortical segmentations: [Link to instructions](https://enigma-infra.github.io/resources/how_to_guides/freesurfer7/){:target="_blank"}
We will apply the FreeSurfer functionalities that are included in the fMRIPrep pipeline. We assume here that you have Apptainer installed as your container platform (see [here](../resources/Container_platforms.md){:target="_blank"} for more info and how to get it).

## Running the subsegmentations: [Link to instructions](https://enigma-infra.github.io/resources/how_to_guides/freesurfer_subseg/)
The subsegmentations pipeline is now ready to be run! Since you’ve all just been through fMRIPrep in Nipoppy, this next step will feel familiar as running this pipeline follows a very similar workflow.

**About the pipeline:**
This pipeline uses existing FreeSurfer 7 functionalities to extract subnuclei volumes from subcortical regions like the *thalamus*, *hippocampus*, *brainstem*, *hypothalamus*, *amygdala*, and *hippocampus*. It requires completed FreeSurfer output (`recon-all`) and integrates the subsegmentation outputs directly into the existing `/mri` and `/stats` directories. Additionally, the pipeline will perform [Sequence Adaptive Multimodal SEGmentation (SAMSEG)](https://surfer.nmr.mgh.harvard.edu/fswiki/Samseg){:target="_blank"} on T1w images in order to calculate a superior intracranial volume.

## Quality Assessment part 1 - running the FS-QC toolbox: [Link to instructions](https://enigma-infra.github.io/resources/how_to_guides/fsqc/){:target="_blank"}
Congratulations, you made it to the quality assessment! For this purpose, we will use FreeSurfer Quality Control (FS-QC) toolbox. The [FS-QC toolbox](https://github.com/Deep-MI/fsqc){:target="_blank"} takes existing FreeSurfer (or FastSurfer) output and computes a set of quality control metrics. These will be reported in a summary table and/or .html page with screenshots to allow for visual inspection of the segmentations.

## Quality Assessment Part 2 - performing a visual quality assessment: [Link to instructions](https://enigma-infra.github.io/resources/how_to_guides/qa/){:target="_blank"}
Quality checking is essential to make sure the output that you have produced is accurate and reliable. Even small errors or artifacts in images can lead to big mistakes in analysis and interpretation, so careful checks help us to verify whether we can savely include a certain region of interest or participant in our analysis. For the FreeSurfer output, we will follow standardized ENIGMA instructions on how to decide on the quality of the cortical and subcortical segmentations.

**At this stage, visual quality assessment of the subsegmentations (e.g., thalamic or hippocampal nuclei) is not required, as there are no established protocols yet and the process would be highly time-consuming; statistical checks (e.g., outlier detection) can be used instead. This may be followed up at a later stage, once there is a project that specifically focuses on these outcomes and the necessary anatomical expertise is available to develop a dedicated quality control manual.**

You can find the updated ENIGMA-PD QC instructions for visual inspection [here](../resources/ENIGMA-PD_visual_QC_instructions.md){:target="_blank"}.

---

## Data sharing
After completing all of the above steps, you're ready to share your derived data with the ENIGMA-PD core team. Please:

- Review the .tsv and Excel spreadsheets for completeness, ensuring all participants are included, there are no missing or unexpected data points, and quality assessment scores have been assigned to each ROI and participant.
- Confirm whether you are authorized to share the quality check .png files. These will be used, along with your quality assessment scores, to help train automated machine learning models for ENIGMA's quality checking pipelines, to eliminate the need for manual checking in the future.

Once these checks are complete, please find the data sharing instructions [here](../../resources/how_to_guides/data_sharing.md).
