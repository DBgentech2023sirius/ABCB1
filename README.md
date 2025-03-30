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
  * <u>ABCB1 optimization</u> - optimization file, used to fit the values of the CYP2C9-optimized model based on the CYP2C9 and ABCB1 experimental data,
  * <u>Final optimization</u> - optimization file, used to fit the model global parameters of the ABCB1-optimized model based on the CYP2C9 and ABCB1 experimental data,
  * <u>E-max model optimization</u> - optimization file, used to fit non-optimized E-max model (get losartan IC<sub>50</sub> curve).
* **Jupyter documents:**
  * <u>Set_values_after_optimizations.ipynb</u> - set values of global and local (in the states) model parameters after each optimization,
  * <u>Optimization_and_identifiability_plots.ipynb</u> - generate plots to compare model predictions with clinical data for all considered genotypes and check model parameters for identifiability,
  * <u>Virtual_population_parameters_distribution.ipynb</u> - distribution of various physiological characteristics of the virtual hypertensive population of 100 [(Kutumova et al., 2022)](https://doi.org/10.3389/fphys.2022.1070115),
  * <u>Sensitivity_analysis.ipynb</u> - perform sensitivity analysis [(Rabitz et al., 1983)](https://doi.org/10.1146/ANNUREV.PC.34.100183.002223) of the model parameters,
  * <u>Pharmacokinetic_analysis.ipynb</u> - perform pharmacokinetic analysis with single value and with normal distribution of the values of each model parameter (between-subject variability),
  * <u>Pharmacodynamic_analysis.ipynb</u> - calculate the _k_block_ values for different doses of losartan potassium and for different genotypes and simulate losartan antihypertensive therapy.
* **Identifiability charts** - identifiability charts for global parameters of the final model.
___
## How to reproduce our model:
1. Go to the [CYP2C9 optimization file](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Optimizations/CYP2C9%20optimization) and initialize the optimization process by clicking on the ”Start optimization process” button;

![Start optimization process](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/Start%20optimization%20process.png?raw=true)

2. After that, you will see an optimization progress bar with the values of the objective and penalty functions, as well as the number of completed evaluations;

![Progress bar](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/Progress%20bar.png?raw=true)

3. After the optimization process is completed, you will see a folder with the CYP2C9 optimization results in the folder with the optimization files;

![CYP2C9 optimization result](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/CYP2C9%20optimization%20result.png?raw=true)

4. In this folder you can find the following files:

![CYP2C9 optimization result files](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/CYP2C9%20optimization%20result%20files.png?raw=true)

* <u>optimizationInfo</u> - optimized values of the model parameters, values of the objective function (calculation deviation) and penalty function (in our case it is equal to 0, since we did not consider additional constraints on the model parameters), and the number of evaluations. **Note** that here we have 2 values of the parameter _k_m_ for each experiment (i.e. for each _CYP2C9_ genotype) since this parameter was considered as local in the CYP2C9 optimization;

![optimizationInfo](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/optimizationInfo.png?raw=true)

* <u>Files whose names end with "plot"</u> contain comparisons between the simulation results after optimization and the experimental data used for it. Such plots are provided for each experiment;

![plot](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/plot.png?raw=true)

* <u>Files whose names end with "chart"</u> are similar to plots, but use a different programming format for use via JavaScript if needed. Such files are provided for each experiment;

![chart](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/chart.png?raw=true)

* <u>Files whose names end with "state"</u> are in a special software format for using optimized values ​​in BioUML diagrams as individual states. Such files are provided for each experiment;

![state](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/state.png?raw=true)

* <u>Files whose names end with "sr"</u> contain numerical results of simulations and are used to create plots in BioUML. Such files are provided for each experiment;

![sr](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/sr.png?raw=true)

5. Now we need to insert the fitted values of the model parameters, obtained during CYP2C9 optimization, into the model. Open [Set_values_after_optimizations.ipynb](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Jupyter%20documents/Set_values_after_optimizations.ipynb) and execute the following cells:
   1. Import libraries,
   2. Initialize functions,
   3. Set values after _CYP2C9_ optimization;
   
![set_values_CYP2C9](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/set_values_CYP2C9.png?raw=true)

6. Now we need to fit the model parameters according to experimental data not only for _CYP2C9_, but also _ABCB1_ genotypes. Go to the [ABCB1 optimization file](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Optimizations/ABCB1%20optimization) and select fitting parameters:
   1. press button "variables" (1),
   2. choose variable (2),
   3. add variable to the fitting set (3);
   4. repeat steps 2 and 3 for the following parameters: _CL_m_, _CL_p_, _Q_, _T_, _V_m_, _Vp_1_, _Vp_2_, _a_, _k_ent_cc_, _k_ent_int_ and _k_int_ent_;

![choose_fitting_parameters](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/choose_fitting_parameters.png?raw=true)

7. Finish setting up the fitting parameters:
   1. press button "Edit" (1),
   2. for k_ent_int parameter set: **Value = 100**, **Upper bound = 1000**, and **Locality = cell lines** (2),
   3. press button "Apply" (3);

![settings_of_fitting_parameters](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/settings_of_fitting_parameters.png?raw=true)

8. Initialize ABCB1 optimization;

![start_ABCB1_optimization](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/start_ABCB1_optimization.png?raw=true)

9. After the optimization process is completed, you will see a folder with the ABCB1 optimization results in the folder with the optimization files;

![ABCB1 optimization result](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/ABCB1%20optimization%20result.png?raw=true)

10. This folder will contain the same file types as after the CYP2C9 optimization (optimizationInfo, plots, charts, states, and sr files);

![ABCB1 optimization result files](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/ABCB1%20optimization%20result%20files.png?raw=true)

11.  **Note**, in optimizationInfo file after ABCB1 optimization we will get 3 values of the parameter _k_ent_int_ for each _ABCB1_ genotype since this parameter was considered as local in the ABCB1 optimization;

![ABCB1 optimizationInfo](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/ABCB1%20optimizationInfo.png?raw=true)

12.  Insert the new fitted values of the model parameters, obtained during ABCB1 optimization, into the model. Open [Set_values_after_optimizations.ipynb](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Jupyter%20documents/Set_values_after_optimizations.ipynb) and execute **"Set values after _ABCB1_ optimization"** cell;

![set_values_ABCB1](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/set_values_ABCB1.png?raw=true)

13. Redefine the values of the model global parameters. Go to the [final optimization](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Optimizations/Final%20optimization) and select fitting parameters:
    1. press button "variables" (1),
    2. choose variable (2),
    3. add variable to the fitting set (3);
    4. repeat steps 2 and 3 for the following parameters: _CL_m_, _CL_p_, _Q_, _T_, _V_m_, _Vp_1_, _Vp_2_, _a_, _k_ent_cc_, and _k_int_ent_;

![settings_of_fitting_parameters_after_ABCB1_opt](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/settings_of_fitting_parameters_after_ABCB1_opt.png?raw=true)

14. Initialize final optimization;

![start_final_optimization](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/start_final_optimization.png?raw=true)

15. After the optimization process is completed, you will see a folder with the final optimization results in the folder with the optimization files. This folder will contain the same file types as after the CYP2C9 and ABCB1 optimizations.

![final optimization result](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/final%20optimization%20result.png?raw=true)

16. Finally, to recieve our model you need open [Set_values_after_optimizations.ipynb](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Jupyter%20documents/Set_values_after_optimizations.ipynb) and execute **"Set values after final optimization"** cell;

![set_values_final](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/set_values_final.png?raw=true)

17. Now you can open [final model](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Diagrams/Final%20model) and test it.

![final_model](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/final_model.png?raw=true)
___
## How to reproduce E-max model (get losartan IC<sub>50</sub> curve):
1. Go to the [E-max model optimization](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Optimizations/E-max%20model%20optimization) and initialize optimization process;

![start_E_max_model_optimization](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/start_E_max_model_optimization.png?raw=true)

2. After the optimization process is completed, you will see a folder with the E-max model optimization results in the folder with the optimization files. To see the curve describing the dependence between _k_block_ and AUC<sub>0-∞, E-3174</sub> open **plot** or **chart**:

![E_max_model_plot](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/E_max_model_plot.png?raw=true)

3. Open **optimizationInfo** to see the optimized coefficients of the E-max model:

![E_max_model_optimizationInfo](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/E_max_model_optimizationInfo.png?raw=true)

4. To insert the optimized coefficients into the E-max model you need open [Set_values_after_optimizations.ipynb](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Jupyter%20documents/Set_values_after_optimizations.ipynb) and execute **"Set values after E-max model optimization"** cell;

![set_values_E_max_model](https://github.com/DBgentech2023sirius/ABCB1/blob/main/Pictures/Instructions/set_values_E_max_model.png?raw=true)

5. Now you can open [optimized E-max model](https://sirius-web.org/bioumlweb/#de=data/Collaboration%20(git)/ABCB1_CYP2C9_losartan_metabolism/Data/Diagrams/Optimized%20E-max%20model) and test it.