# Multiple Symptom Progression Modelling project

## Project team

<div class="grid cards" markdown>
  
- ![](../../assets/profile_pictures/boris.jfif){ width="120" }  
  **Boris Gutman**<sup>1</sup> (PI)  
  
- ![](../../assets/profile_pictures/marco.jfif){ width="120" }  
  **Marco Lorenzi**<sup>2</sup> (PI)
  
- ![](../../assets/profile_pictures/emile.jpg){ width="120" }  
  **Emile d'Angremont**<sup>3</sup> (Postdoc)

- **Daniel Semchin**<sup>1</sup> (Graduate student)
  
- ![](../../assets/profile_pictures/ysbrand.jpg){ width="120" }  
  **Ysbrand van der Werf**<sup>3</sup> (PI)  

- ![](../../assets/profile_pictures/jb.jpg){ width="120" }  
  **Jean-Baptiste Poline**<sup>4</sup> (PI)  

- ![](../../assets/profile_pictures/michelle.jpg){ width="120" }
  **Michelle Wang**<sup>4</sup> (PhD student)  

</div>

---

<sup>1</sup>*Illinois Institute of Technology, Department of Biomedical Engineering, Chicago, United States of America*  
<sup>2</sup>*Inria Center of Université Côte d’Azur, Valbonne, France*
<sup>3</sup>*Amsterdam UMC location Vrije Universiteit Amsterdam, Department of Anatomy and Neurosciences, Amsterdam, the Netherlands*  
<sup>4</sup>*NeuroDataScience - ORIGAMI laboratory, McConnell Brain Imaging Centre, The Neuro (Montreal Neurological Institute-Hospital), Faculty of Medicine, McGill University, Montreal, Quebec, Canada*  


## Multi-Symptom Progression Modelling

### Project summary

Our aim is to identify differential disease progression trajectories in heterogeneous longitudinal cohorts, based on specific clinical and neuroimaging biomarkers. Currently, we include derived data from FreeSurfer 7 processing, but we are working on extending this with derived data from the WML pipeline and/or TBSS pipeline. Required clinical data are MoCA and MDS-UPDRS-III.

Read more about this project in the full [secondary proposal](../../assets/secondary_proposals/ENIGMA_Secondary_Proposal_MultisymptomProgressionModel.pdf).

Link to repositories:

- [DP-MoSt](https://gitlab.inria.fr/aviani/dpmost)

- [COMIND](https://github.com/dsemchin/COMIND/tree/main)

## Federated Learning subproject

### Project summary

Many neuroimaging datasets, especially those involving clinical populations, cannot easily be shared between research groups. In those situations, decentralized multisite analyses can be conducted using federated learning (FL) techniques. In FL, local models are fitted at each site, and fitted model parameters are shared and aggregated; participant-level data always remain local, thus respecting data privacy constraints. In this subproject, we will set up a multisite federated learning network of Parkinson’s disease datasets and conduct decentralized statistical harmonization and disease progression modelling with neuroimaging and clinical data.

Link to Github repository:

- [FL-PROG](https://github.com/neurodatascience/fl-prog)






