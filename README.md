# GPCR_AlphaFold

This repository provides the implementation of the paper - "**Characterizing the Conformational States of G Protein Coupled Receptors Generated with AlphaFold**". 
This project conducts an evaluation of AlphaFold’s performance in predicting GPCR structures and their conformational states by comparing its predictions to experimentally determined structures. 

The data for the ground truth GPCRs can be found here - [TM Only Final Data](https://github.com/garimachib01/GPCR_AlphaFold/tree/main/Data/TM_only_final)

Data for AlphaFold 2 generated structures can be found here - [AlphaFold 2 Data](https://github.com/garimachib01/GPCR_AlphaFold/tree/main/Data/AF2_Aligned)

Data for AlphaFold 3 generated structures can be found here - [AlphaFold 3 Data](https://github.com/garimachib01/GPCR_AlphaFold/tree/main/Data/AF3_aligned)

To reproduce results, clone this GitHub repository and install the following packages in Python: 

`pip install biopython`

 `pip install mdtraj`
 


## Evaluating AlphaFold predictions
- ### Average Deformation
  `calculating_deformation.ipynb` contains details on how to calculate the average distance between alpha-carbon atoms of reference and AlphaFold generated structures.
  Change file paths to get deformations for AlphaFold 2 and AlphaFold 3 accordingly
- ### Helix 3 - Helix 6 Distance
  `h3_h6.ipynb` contains the code to calculate the H3-H6 distance, an important metric that is correlated with the activity level of GPCRs. Calculating the difference between the H3-H6 distance in reference and generated structures can give us an indication of AlphaFold's predictive accuracy. Change file paths for AlphaFold 2 and AlphaFold 3 accordingly.

- Additionally, `calculate_overlapping_sequence_ratio.ipynb` shows an example of how to calculate the ratio of sequence overlap between the reference and AlphaFold 2 generated structures.

## Results
The [Results](https://github.com/garimachib01/GPCR_AlphaFold/tree/main/Results) folder contains the average deformation and the H3-H6 distances. The final results for AlphaFold 2 and AlphaFold 3 can be found in `deform_h3_h6_results_AF2.csv ` `and deform_h3_h6_results_AF3.csv` respectively.

## Plots
Refer to `plots.ipynb` for details on the plots provided in the paper. Change file paths for AlphaFold 2 and AlphaFold 3 accordingly. 

  
