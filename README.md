# Two-stage feature selection for machine learning-aided DFT-based surface reactivity study on single-atom alloys
Viejay Z. Ordillo, Koji Shimizu, Darwin B. Putungan, Alexandra B. Santos-Putungan, Satoshi Watanabe, Rizalinda L. de Leon, Joey D. Ocon, Karl Ezra S. Pilario, and Allan Abraham B. Padama

https://doi.org/10.1088/1361-651X/ad53ee

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Abstract
This paper presents a feature-centric strategy for predicting adsorption energies of key CO2 reduction reaction (CO2RR) adsorbates, CO and H species, utilizing density functional theory-based calculations for eight adsorption sites and considering alloying effects of nine transition metals at single-atom concentrations. Here, we explore a class of materials consisting of a majority host metal where individual atoms of a different element are dispersed called single-atom alloys (SAA). A total of eight feature selection methods are assessed within Gradient Boosting Regression and Linear Regression models. This study proposes a practical and effective two-stage approach that narrows down the initial 86 features to subsets of 10 and 7 for CO and H adsorption energy predictions, respectively, with the arithmetic mean of valence electrons (VE-am) feature consistently emerging as highly influential, validated through permutation and Shapley additive explanations-based feature importance analyses. The models exhibit robust performance on unseen data, indicating their generalization capability. The findings emphasize VE-am as a potential key machine learning feature for CO2RR on SAA surfaces and underline the effectiveness of the feature-centric approach in understanding feature impacts in machine learning models for CO2RR on SAA systems. Additionally, while other features based on structural, electronic and elemental properties may not individually impact the model significantly, their collective contribution plays a vital role in achieving more accurate adsorption energy predictions.

## Installation

You can download the data used in this study by cloning the git repository:
   ```sh
   git clone {LINK TO REPO}
   ```

[//]: # (To install the required packages, use)

[//]: # (   ```sh)

[//]: # (   pip install -r requirement.txt)

[//]: # (   ```)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Computational Details


> ### DFT-based Calculations
> **Software**: Quantum Espresso ver. 6.5
>
> **Pseudopotential**: Ultrasoft
>
> **K-points**: (4 x 4 x 1) and (12 x 12 x 12) Monkhorst-Pack k-points meshes for Surface and Bulk models, respectively.
>
> **Energy Cutoff**: 600 eV
>
> **Force Convergence Threshold**: 0.03 eV/Å
>
> **Energy Convergence Threshold**: 1x10-5 eV
>
>
>
> **Transition Metals**: Co, Ni, Cu, Rh, Pd, Ag, Ir, Pt, Au
>
> **Slab Model**:  3x3x4 supercell of the (111) facet, with 15 Å vacuum layer (shown in the figure below):
>
>   * (a) pure surface
>
>   * (b) SAA - dopant is in the first layer
>
>
> **Adsorbates**: CO and H
>
> **Adsorption Sites**: hcp(h1 and h2), top(t1 and t2), bridge(b1 and b2), fcc(f1 and f2)
>

> ### Machine Learning
> #### **Features**: All features used in this study are presented in Table S1 of the Supplementary Information document.
> #### **Base ML Algorithms**: Gradient Boosting Regression and Ordinary Least Squares (Linear) Regression
> #### **Hyperparameter Optimization**: Grid Search (Linear Regression) and Bayesian Optimization (Gradient Boosting Regression)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- LICENSE -->
## Citation

Ordillo, V., Shimizu, K., Putungan, D.B., Santos-Putungan, A.B., Watanabe, S., de Leon, R., Ocon, J.D., Pilario, K.E. and Padama, A.A.B., 2024. Two-Stage Feature Selection for Machine Learning-aided DFT-based Surface Reactivity Study on Single-Atom Alloys. Modelling and Simulation in Materials Science and Engineering.
<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact
Allan Abraham B. Padama, Ph.D. (abpadama@up.edu.ph)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

This work was primarily funded by the Department of Science and Technology—Philippine Council for Industry, Energy, and Emerging Technology Research and Development (DOSTPCIEERD) with Project No. 10128 in 2022. This project is under the East Asia Science and Innovation Area Joint Research Program (e-ASIA JRP) titled ‘Computational Design of High Entropy Alloys for Catalyst and Battery Applications’. All calculations were performed using the computing facilities of the Watanabe Laboratory of The University of Tokyo, the Computing and Archiving Research Environment of DOST—Advanced Science and Technology Institute, the Institute of Mathematical Sciences and Physics of the University of the Philippines Los Ba ̃nos, and the supercomputer Fugaku by RIKEN.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
