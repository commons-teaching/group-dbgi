# Metabolomic study on _Derris elliptica_,  _Erythroxylum coca_ and _Strophanthus hispidus_
SBL.20004   
  
Report 09.06.2025 

### Group DBGI  
  
- Michele Cereghetti  
- Tanguy Schmidt  
- Jonas Hendricks  

## Introduction
Throughout evolution, plant species have developed different traits to adapt and survive in response to environmental pressures. One known strategy is the production of specialized metabolites, which often serve as  defenses by making the plant unpalatable or toxic to herbivores. They can also be useful for attracting pollinators, allelopathy, attracting and selecting microorganisms,... These metabolites not only play a vital role in plant survival, but they have also long attracted human interest. Over time, humans observed and studied plants, gradually recognizing their unique properties and harnessing them primarily for food and medicine, and in some cases, even for fishing or hunting. Today, the field of metabolomics seeks to investigate and understand these specialized compounds, exploring how plants use them to interact with their environment and defend themselves.   
  
In many tropical regions, indigenous communities still live in close relationship with nature and rely on plant-derived metabolites for surviving and hunting. In this context, our study focused on three tropical plant species of particular interest: _Derris elliptica_, _Erythroxylum coca_, and _Strophanthus hispidus_. These plants belonging to different genera are known for producing bioactive molecules with pharmacological interest and for their use in indigenous communities.
  
[_Derris ellipctica_](https://en.wikipedia.org/wiki/Derris_elliptica) is a plant native to Southeast Asia, particularly found in Indonesia, Malaysia and the Philippines. This plant is well-known for containing a potent flavonoid called [rotenone](https://www.wikidata.org/wiki/Q412388) in its roots. Indigenous communities use this metabolite by crushing the roots and releasing them into water to stun and gather fishes. Moreover _Derris elliptica_ is also employed in traditional medicine to treat various conditions like bleeding, toothaches or stomachaches[^1]. Rotenone has also been studied for its pesticidal properties however its use has declined mainly due to concerns about its suspected link to Parkinson's disease. This plant remains an important example of how natural metabolites can be useful in traditional societies[^2].
  
[_Erythroxylum coca_](https://it.wikipedia.org/wiki/Erythroxylum_coca) is a plant native to South America. It is a small shrub that can reach 3 meters in height and grows in humid forests. It is known worldwide to be the source of a psychoactive alkaloid, [cocaine](https://www.wikidata.org/wiki/Q41576). This metabolite present in the leaves of the plant is used as a narcotic, but it also for anesthetic properties in medical applications. _Erythroxylum coca_ was also used for the production of liqueurs and drinks. The original recipe for "Coca-Cola" and some wines were flavored by adding the leaves of the plant.

[_Strophantus Hispidus_](https://en.wikipedia.org/wiki/Strophanthus_hispidus) belonging to the genus _Strophantus_ and family of _Apocyaceneae_ is native to the african continent and common in tropical regions as well as savannah forests predominantly in Ghana, Senegal, Sudan, Congo DR, Uganda, and Tanzania[^3]. Local names for the plants are differing and there are more than 40 names commonly known in West-Africa often referring to its poisenous compounds[^4]. Most well known is the plants use as an arrow poison[^5]. The plant also has its use for traditional medicinal applications, as such Agyara et al. have proven its antimicrobial, antioxidant, and enhanced wound healing properties. In western Europe the plant found its use as a heart stimulant and to treat hypotension and some arrhythmias[^6]. The main group of characteristic compounds found in _Strophantus hispidus_ are the _strophantines_ also known as [ouabain](https://www.wikidata.org/wiki/Q60074861) belonging to the group of _cardinolides_ and cardiac glycosides.

The objective of this study is to use metabolomics to confirm the presence of the known bioactive metabolites produced by these three plants and to try to define similarities and differences they possess among each other.

## Material and Methods
### Samples collection
In our study, samples from the three plants were collected from the tropical greenhouse of Jardin de Botanique de l'Université de Fribourg. Pictures of the plants were taken and uploaded in the DGBI project in the iNaturalist domain ([_Derris ellipctica_](https://www.inaturalist.org/observations/117770419), [_Erythroxylum coca_](https://www.inaturalist.org/observations/208861685) and [_Strophantus Hispidus_](https://www.inaturalist.org/observations/117770425) ). Samples were collected using sterile scalpels to cut one or two plant leaves. Tissues were placed inside a 50 mL Falcon tube and immediately frozen in liquid nitrogen to minimize alterations of their metabolomes caused by the gathering.

### Samples preparation
Falcon tubes are reopened in the laboratory. Due to the drop in temperature, the leaves were broken. Therefore, we collected fragments of plant tissue to a weight of about 150 ug for every plant. Fragments were then placed in an Eppendorf and 1.5 mL of solvent (80% de méthanol, 20% d'eau et 0.2% d'acide formique) was added to it. To it, we added 2 or 3 metal spheres and then inserted the samples into the Retsch machine for 3 minutes to break the tissues into smaller fragments and extract metabolites. Thereafter, the samples were centrifuged to settle the solid particles. thus 1 mL of supernatant was taken and placed in special glass tubes. 

### LCMS analysis
Liquid chromatography followed by mass spectrometry analysis (LC-MS) was used to analyze the samples. It consists on a first part with the use of an ultra high-performance liquid chromatography (UPLC), a more sensitive and rapid version of HPLC. The molecules are then separated via a reverse-phase column according to their polarity. Then the samples are injected inside the mass spectrometer, where an MS/MS analysis is performed to obtain information about the metabolites present. The mass spectrometer used for this experiment is a Q-orbitrap.

[LC conditions](https://github.com/commons-teaching/SBL.20004.2024/blob/main/lc_conditions.txt)

[MS conditions ](https://github.com/commons-teaching/SBL.20004.2024/blob/main/ms_conditions.txt)

### Data treatment
The data obtained from the LCMS were converted to a format supported do by the MZmine program (like [ProteoWizard](https://proteowizard.sourceforge.io/)) and through this software were analyzed. Then the data were processed in this order to obtain the features list of our samples: 
- Mass pick detection. In this initial step, the peaks from the spectrometry data are identified, identifying the true peaks and removing the noise.
- Chromatogram building. A chromatogram (XIC/EIC) is created for each detected ion. This allows the visualization of how the ion’s intensity changes over time, showing its retention time.
- Chromatogram deconvolution. Here peaks are identified and separated in the chromatogram.
- Isotope grouping. In this penultimate step, the isotopes of each ion are grouped into a single feature. in this way, the moinoisomeric mass of the feature can be obtained.
- Feature alignment. The last step allows aligning the features detected in each sample to compare their different intensities.

With these processed data and metadata, a molecular network with [Cytoscape](https://cytoscape.org/) was created to cluster and visualize the detected features. 


## Results

### MS1
After the features allignment step we obtain 5839 features in the [final peak list](https://github.com/commons-teaching/group-dbgi/blob/main/aligned_feature_list.csv).  
By not taking blanks into account you get 5694 features that can be viuslized [here](https://github.com/commons-teaching/group-dbgi/blob/main/aligned_feature_list_samples2.csv). 
![Derris elliptica overview](https://github.com/user-attachments/assets/25acb808-9246-4eb4-8d0c-7ddda1d1bf58)  
Overview of the network of _Erythroxylum coca_
![Erythroxylum coca overview](https://github.com/user-attachments/assets/cf480e9e-a28e-4424-aebc-5d6801e537c8)
Overview of the network of _Strophanthus hispidus_
![Strophanthus hispidus overview](https://github.com/user-attachments/assets/17cfb7fb-b181-4721-8a9f-0e97eda07ddc)Overview of the network of _Derris elliptica_  





  
![newplot](https://github.com/user-attachments/assets/e425f651-f06a-4818-aa0f-aeb042f4564c)
Metabolites heatmap  

Concerning _Derris ellipctica_ we were unable to find features related to rotenone in the nodes network.  
![Derris elliptica cluster 1](https://github.com/user-attachments/assets/e1b1b684-1d8c-4970-8d92-aeed0855f2da)
Cluster 1  
![Derris elliptica cluster 1 strucutre 1a](https://github.com/user-attachments/assets/36748ce0-b8a2-49a9-9e49-ce81595a9567)![Derris elliptica cluster 1 strucutre 1b](https://github.com/user-attachments/assets/60e79c10-806f-4667-84a5-f3fbd9218442)
Structure of Clerodendrin and Eriodictyol  
![Erythroxylum coca cluster cocaine](https://github.com/user-attachments/assets/41beab70-d4f7-4ef3-ab3b-2657a1630624)
Cluster 2  
![Erythroxylum coca structure cocaine](https://github.com/user-attachments/assets/16161141-1044-42cb-8255-0bf7632ae244)
Structure of cocaine  
![Strophanthus hispidus cluster Strophanthidin ](https://github.com/user-attachments/assets/70b40da8-d61c-43ce-8b47-0f15b7e0f69a)
Cluster 3  
![Strophanthus hispidus structureStrophanthidin ](https://github.com/user-attachments/assets/f6451cd4-8a3d-4821-8133-d8dc26c8ed36)
Structure of strophanthidin  

## Conclusion
## References
[^1]: Khan, M. R., Omoloso, A. D., & Barewai, Y. (2006). Antimicrobial activity of the Derris elliptica, Derris indica and Derris trifoliata extractives. Fitoterapia, 77(4), 327-330. 
[^2]: Ling, Nicholas. (2003). Rotenone - A review of its toxicity and use for fisheries management. Science for Conservation. 211. 1-40. 
[^3]:Agyare, C., Dwobeng, A. S., Agyepong, N., Boakye, Y. D., Mensah, K. B., Ayande, P. G., & Adarkwa-Yiadom, M. (2013). Antimicrobial, antioxidant, and wound healing properties of Kigelia africana (Lam.) Beneth. and Strophanthus hispidus DC. Advances in Pharmacological and Pharmaceutical Sciences, 2013(1), 692613.
[^4]:Burkill, H. M. (1985). The useful plants of West Tropical Africa, vol. 1. Royal Botanic Gardens, Kew, 343.
[^5]:Fraser, T. R. (1890). XXI.—Strophanthus hispidus: its Natural History, Chemistry, and Pharmacology. Transactions of the Royal Society of Edinburgh, 35(4), 955–1027. doi:10.1017/S0080456800008589
[^6]:Fürstenwerth, H. (2010). Ouabain-the insulin of the heart. International journal of clinical practice, 64(12), 1591.

