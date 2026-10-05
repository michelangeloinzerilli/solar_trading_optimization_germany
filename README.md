# Renewable Energy Trading Optimization

Integrated Project of the Year developed in collaboration with **TokWise**, focusing on the optimization of solar PV trading strategies in the German electricity market.

## Overview

This project investigates how **economic curtailment, multi-market trading and battery storage** can improve the revenues of utility-scale solar PV assets.

A sequential optimization framework was developed to simulate trading decisions across:

- **aFRR balancing markets**
- **Day-Ahead (DA) market**
- **Intraday (ID) market**

The model evaluates how renewable asset owners can optimally allocate available generation while accounting for changing market prices, generation forecasts, curtailment opportunities and storage flexibility.

## Methodology

A **Mixed-Integer Linear Programming (MILP)** framework was developed in Python to maximize PV asset revenues through sequential market participation.

Different configurations were evaluated:

- **2-stage model:** Day-Ahead + Intraday
- **3-stage model:** aFRR + Day-Ahead + Intraday
- **No-curtailment scenario:** all available generation must be traded
- **Battery scenarios (`_Battery`):** co-located BESS integrated into the trading strategy
- **Future market scenarios:** increased negative prices and higher price volatility

The models use real German electricity-market and solar-generation data provided by TokWise together with additional external market datasets.

## Repository Structure

### Datasets

To evaluate each of the scenarios, the following dataset names must be changed directly in the given notebooks.

- **`full_dataset_ino_energy_final.parquet`**  
  Original dataset provided by TokWise.

- **`filtered_solar_data.parquet`**  
  Filtered TokWise dataset containing the variables required by the optimization models.

- **`filtered_solar_data_augmented_realistic.parquet`**  
  Extended dataset used to simulate higher Day-Ahead price volatility and future market conditions.

### Jupyter Notebooks

The notebooks contain the different optimization scenarios studied.

Naming conventions indicate the model configuration:

- **`2 stages`** → Day-Ahead + Intraday optimization
- **`3 stages`** → aFRR + Day-Ahead + Intraday optimization
- **`no curtailment`** → curtailment is not allowed
- **`_Battery`** → battery storage is included in the optimization

### `inputs/`

Contains additional input data either:

- provided by the industry partner,
- or obtained from external public sources.

## Technologies

**Python · MILP · Jupyter Notebook · Pandas · NumPy · Electricity Market Optimization · Battery Storage**

## Report

The complete project report is available in the repository.

The work was developed as the **Renewable Energy Trading Optimization (RETO)** Integrated Project of the Year in partnership with TokWise.

## License

Copyright © 2026. All rights reserved.

This repository is made publicly available for **portfolio and academic viewing purposes only**. No permission is granted to copy, modify, distribute, or reuse the original code, reports, models, or other materials developed by the project authors without prior written permission.

Datasets and other materials provided by **TokWise** or obtained from external sources remain subject to the rights, licenses and restrictions of their respective owners.

## Project Team

This project was developed by an international student team as part of the **InnoEnergy SELECT Master's programme**, in collaboration with **TokWise**.

**Michelangelo Inzerilli**  
EIT InnoEnergy, KTH Royal Institute of Technology and Universitat Politècnica de Catalunya