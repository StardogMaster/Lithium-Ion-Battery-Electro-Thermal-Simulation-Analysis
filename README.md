# Lithium-Ion-Battery-Electro-Thermal-Simulation-Analysis
This is a simulation and analysis project for lithium battery performance. Based on a second-order RC electrical-thermal coupling model and real battery datasets, it can reproduce the operational characteristics and performance degradation patterns of lithium batteries under various scenarios.

## Project Overview
This project focuses on simulating and analyzing lithium-ion battery behavior under real-world scenarios, with core functions:
1. Second-order RC electro-thermal coupling simulation (voltage/temperature/current during discharge)
2. NASA battery dataset calibration (capacity decay & impedance growth)
3. Battery model parameter estimation
4. Nonlinear current demand analysis ("death spiral" effect)
5. Runtime sensitivity analysis (power/temperature/aging impact)
6. Cross-validation of simulation results


## Project Structure
projection/
├── Source Codes/
│   ├── battery_thermal_rc_model.py          # 2nd-order RC electro-thermal coupling battery model: Simulate voltage, temperature and current during discharge
│   ├── electrothermal_coupling.py           # Simplified electro-thermal coupling model: Verify the coupling relationship of current-temperature-internal resistance
│   ├── nasa_metadata_cleaning.py            # NASA battery dataset processing: Data cleaning and preprocessing for aging indicators
│   ├── nasa_calibration_seaborn.py          # NASA data calibration: Fitting for battery capacity decay and impedance growth
│   ├── parameter_estimation.py              # Battery model parameter identification: Estimate RC network and aging coefficient parameters
│   ├── power_nonlinearity_analysis.py       # Power nonlinearity analysis: Verify the "voltage drop → current surge" death spiral effect
│   ├── sensitivity_analysis.py              # Runtime sensitivity analysis: Analyze power/temperature/aging impact on battery life
│   └── cross_validation.py                  # Model cross-validation: Verify the reliability of simulation results
├── Data Files/
│   ├── metadata.csv                         # NASA B0005 battery test data: Capacity, impedance and other aging indicators
│   ├── user_behavior_dataset.csv            # Mobile phone user behavior data: Screen-on time, daily battery drain, etc.
│   ├── RedmiK70pro.csv                      # Redmi K70 Pro battery experimental data: Physical parameters and test results
│   ├── data3.csv                            # Supplementary battery test data: Auxiliary calibration and verification
│   └── Mobiles Dataset(2025).csv            # 2025 multi-model mobile phone battery dataset: Cross-device performance comparison
└── Output Figures/
    ├── Fig1_Voltage.png                     # Voltage comparison curve: New battery vs aged battery terminal voltage
    ├── Fig2_Temperature.png                 # Temperature evolution curve: Battery temperature change during discharge
    ├── Fig3_Current.png                     # Discharge current curve: With avalanche effect annotation
    ├── nasa_calibration_seaborn.png         # NASA calibration result: Fitted capacity decay and impedance growth curve
    ├── parameter_identification_seaborn.png # Parameter estimation chart: Fitting result of RC model parameters
    └── power_nonlinearity_analysis.png      # Nonlinear analysis chart: Voltage-dependent current surge curve

## Data Description
File Name	                                            Description
metadata.csv	            NASA B0005 battery test data (capacity, impedance, cycle number)
user_behavior_dataset.csv	Mobile user behavior data (screen-on time, battery drain per day)
RedmiK70pro.csv	            Experimental Use of Redmi K70 Pro
Mobiles Dataset(2025).csv	2025 multi-model mobile battery dataset (for cross-device comparison)
