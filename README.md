# Modeling the effect of _CYP2C9_ and _ABCB1_ polymorphisms on the pharmacokinetics and pharmacodynamics of losartan
Model is able to predict the profiles of both losartan and its active metabolite, E-3174, based on the _CYP2C9_ and _ABCB1_ genotypes of a particular patient simultaneously.

Considered  _CYP2C9_ genotypes are _CYP2C9\*1/CYP2C9\*1_ and _CYP2C9\*3/CYP2C9\*3_;<br>
Considered  _ABCB1_ genotypes are GG/CC, GT/CT, and TT/TT.

![model_scheme_BioUML_eng](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/model_scheme_BioUML_eng.jpg?raw=true)

You can download both initial model [(Babaev et al., 2024)](https://doi.org/10.17537/2024.19.533) and our model in SBML format to verify them in other software packages.
Also you can test our model in [BioUML](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Diagrams/Final%20model) software. In provided project you can find all files to reproduce our model:
* **Diagrams:**
    * <u>Babaev2024 - CYP2C9 variants</u> - initial model describing pharmacokinetics of losartan in relation to different _CYP2C9_ alleles,
    * <u>Non-optimized model</u> - model with Enterocyte compartment with non-optimized values of the parameters,
    * <u>CYP2C9-optimized model</u> - model with Enterocyte compartment with values of the parameters optimized only on _CYP2C9_ data; values of the _k_m_ parameter (CYP2C9 activity) are incorporated in states,
    * <u>ABCB1-optimized model</u> - model with Enterocyte compartment with values of the parameters optimized on _CYP2C9_ and _ABCB1_ data; values of the _k_m_ (CYP2C9 activity) and _k_ent_int_ (ABCB1 activity) parameters are incorporated in states,
    * <u>Final model</u> - the same model as ABCB1-optimized model with the refined values of global parameters, with equations for pharmacokinetic analysis, and with units,
    * <u>Final model (for population)</u> - the same as the final model, but used for pharmacokinetic analysis with between-subject variability,
    * <u>Non-optimized E-max model</u> - a model to describe the dependence between _k_block_ and AUC<sub>0-∞, E-3174</sub> with non-optimized values of the parameters,
    * <u>Optimized E-max model</u> - a model to describe the dependence between _k_block_ and AUC<sub>0-∞, E-3174</sub> with optimized values of the parameters,
    * <u>CVS model</u> - a model of the human <u>cardiovascular</u> and <u>renal</u> systems [(Kutumova et al., 2022)](https://doi.org/10.3389/fphys.2022.1070115).
* **Tables:**
  * <u>CYP2C9\*1_CYP2C9\*1 val data</u> - experimental data for model validation for _CYP2C9\*1/CYP2C9\*1_ genotype [(J. Bae et al., 2011)](https://doi.org/10.1038/aps.2011.100),
  * <u>CYP2C9\*3_CYP2C9\*3 val data</u> - experimental data for model validation for _CYP2C9\*3/CYP2C9\*3_ genotype [(J. Bae et al., 2011)](https://doi.org/10.1038/aps.2011.100),
  * <u>GG_CC val data</u> - - experimental data for model validation for GG/CC genotype [(Shin et al., 2020)](https://doi.org/10.1007/s12272-020-01294-3),
  * <u>GT_CT val data</u> - - experimental data for model validation for GT/CT genotype [(Shin et al., 2020)](https://doi.org/10.1007/s12272-020-01294-3),
  * <u>TT_TT val data</u> - - experimental data for model validation for TT/TT genotype [(Shin et al., 2020)](https://doi.org/10.1007/s12272-020-01294-3),
  * <u>Virtual_hypertensive_population_of_100</u> - virtual hypertensive population of 100 patients [(Kutumova et al., 2022)](https://doi.org/10.3389/fphys.2022.1070115),
  * <u>CYP2C9\*1_CYP2C9\*1 Swedish data</u> - experimental data for the comparison of losartan and E-3174 profiles from the study in Swedish patients [(Yasar et al., 2002)](https://doi.org/10.1067/mcp.2002.121216),
  * <u>CYP2C9\*1_CYP2C9\*1 Chinese data</u> - experimental data for the comparison of losartan and E-3174 profiles from the study in Chinese patients [(Li et al., 2009)](https://doi.org/10.1080/00498250903134435),
  * <u>Scaled sensitivities for CYP2C9\*1_CYP2C9\*1 and GG_CC</u> - scaled sensitivities for the parameters of the final model with _k_m_ and _k_ent_int_ values corresponding to _CYP2C9\*1/CYP2C9\*1_ and GG/CC genotypes, respectively,
  * <u>Scaled sensitivities for CYP2C9\*1_CYP2C9\*1 and GT_CT</u> - scaled sensitivities for the parameters of the final model with _k_m_ and _k_ent_int_ values corresponding to _CYP2C9\*1/CYP2C9\*1_ and GT/CT genotypes, respectively,
  * <u>Scaled sensitivities for CYP2C9\*1_CYP2C9\*1 and TT_TT</u> - scaled sensitivities for the parameters of the final model with _k_m_ and _k_ent_int_ values corresponding to _CYP2C9\*1/CYP2C9\*1_ and TT/TT genotypes, respectively,
  * <u>Unscaled sensitivities for CYP2C9\*1_CYP2C9\*1 and GG_CC</u> - unscaled sensitivities for the parameters of the final model with _k_m_ and _k_ent_int_ values corresponding to _CYP2C9\*1/CYP2C9\*1_ and GG/CC genotypes, respectively,
  * <u>Unscaled sensitivities for CYP2C9\*1_CYP2C9\*1 and GT_CT</u> - unscaled sensitivities for the parameters of the final model with _k_m_ and _k_ent_int_ values corresponding to _CYP2C9\*1/CYP2C9\*1_ and GT/CT genotypes, respectively,
  * <u>Unscaled sensitivities for CYP2C9\*1_CYP2C9\*1 and TT_TT</u> - unscaled sensitivities for the parameters of the final model with _k_m_ and _k_ent_int_ values corresponding to _CYP2C9\*1/CYP2C9\*1_ and TT/TT genotypes, respectively,
  * <u>Normal distribution of model parameters (300)</u> - 300 values of each model parameter obtained from the normal distributions,
  * <u>Antihypertensive effect</u> - systolic and diastolic blood pressure responses of virtual hypertensive population of 100 with different _ABCB1_ genotypes for daily oral doses of 50 and 100 mg losartan potassium,
  * <u>k_blocks</u> - _k_block_ values for different _ABCB1_ genotypes for oral doses of 50 and 100 mg losartan potassium,
  * <u>AUC for various time intervals</u> - area under the concentration time-curve (AUC) values for losartan + E-3174 together for various time intervals, for different _ABCB1_ genotypes, and for oral dose of 50 mg losartan potassium,
  * <u>AUC_E-3174 for 25 50 100 mg losartan</u> - area under the concentration time-curve (AUC) values from 0 to infinity for E-3174 for 25, 50, and 100 mg oral doses of losartan potassium for _CYP2C9\*1/CYP2C9\*1_ and GG/CC combined genotype to create IC<sub>50</sub> curve,
  * <u>Pharmacokinetic analysis result</u> - key pharmacokinetic parameters values for different _ABCB1_ genotypes after an oral dose of 50 mg losartan potassium,
  * <u>Pharmacokinetic analysis result (for population)</u> - 300 values of _C_<sub>max</sub>, _t_<sub>max</sub>, and AUC<sub>0-∞</sub> for different _ABCB1_ genotypes after an oral dose of 50 mg losartan potassium.
* **Optimizations:**
  * <u>CYP2C9 optimization</u> - optimization file, used to fit the values of the non-optimized model based on the CYP2C9 experimental data,
* **Jupyter documents:**
  * <u>Set_values_after_optimizations.ipynb</u> - set values of global and local (in the states) model parameters after each optimization,
  * <u>Optimization_and_identifiability_plots.ipynb</u> - generate plots to compare model predictions with clinical data for all considered genotypes and check model parameters for identifiability,
  * <u>Virtual_population_parameters_distribution.ipynb</u> - distribution of various physiological characteristics of the virtual hypertensive population of 100 [(Kutumova et al., 2022)](https://doi.org/10.3389/fphys.2022.1070115),
  * <u>Sensitivity_analysis.ipynb</u> - perform sensitivity analysis [(Rabitz et al., 1983)](https://doi.org/10.1146/ANNUREV.PC.34.100183.002223) of the model parameters,
  * <u>Pharmacokinetic_analysis.ipynb</u> - perform pharmacokinetic analysis with single value and with normal distribution of the values of each model parameter (between-subject variability),
  * <u>Pharmacodynamic_analysis.ipynb</u> - calculate the _k_block_ values for different doses of losartan potassium and for different genotypes and simulate losartan antihypertensive therapy.
* **Identifiability charts** - identifiability charts for global parameters of the final model.
___
## How to reproduce our results:
1. Go to the [CYP2C9 optimization file](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Optimizations/CYP2C9%20optimization) and initialize the optimization process by clicking on the ”Start optimization process” button;

![Start optimization process](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/Start%20optimization%20process.png?raw=true)

2. After that, you will see an optimization progress bar with the values of the objective and penalty functions, as well as the number of completed evaluations;

![Progress bar](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/Progress%20bar.png?raw=true)

3. After the optimization process is completed, you will see a folder with the CYP2C9 optimization results in the folder with the optimization files;

![CYP2C9 optimization result](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/CYP2C9%20optimization%20result.png?raw=true)

4. In this folder you can find the following files:

![CYP2C9 optimization result files](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/CYP2C9%20optimization%20result%20files.png?raw=true)

   1. dddcc
   2. пппп
   3. ааа