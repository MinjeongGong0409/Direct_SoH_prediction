# Direct_SoH_prediction

## Introduction
Diagnostic protocol data for 18650 cylindrical battery, corresponding state of charge (SoH) data, and codes for direct SoH prediction.
The dataset consists of diagnostic protocol classification and SoH regression data at 188 and 1048 SoH values.

## Summary of the cells
The used cell is 18650 cylindrical cell (Samsung, INR18650-29E, 2.85 Ah) with NCA/Graphite.
The cells were degraded under diverse C-rate conditions (charge: 0.5, 1.0, 2.0/discharge: 0.5, 1.0, 2.0, 4.0), and 3 cells per degradation condition were used.

To confirm expandability, 2 types of 21700 cylindrical cell data were collected.
  1) 21700 cell 1: Samsung, INR21700-50E, 4.9 Ah, NCA/Graphite+Si
  2) 21700 cell 2: LG, INR21700-M50LT, 4.8 Ah, NCM/Graphite
These cells were cycled under 0.5 C-rate charge and 1.0 C-rate discharge, and protocol data were collected every 100 cycles.
 
## Battery data overview
The raw data of diagnostic protocol data are stored in 'raw_data_SoH_protocol_X.zip' (X = 1, 2, 3, 4, 5).
It consists of all protocol data measured at a specific cycle, and each protocol data includes the voltages at each current pulse and rest time (1.65, 2.0 C-rate charge and discharge current pulse for 5 seconds and rest times between every current pulse)

The calculated features from raw_data_SoH_protocols are stored in 'Calculated features.zip'. There are initila/final voltage at each current pulse and rest time, resistance, IR drop, skewness, and kurtosis. In addition, the ratio of resistance, or hysteresis also calculated.

21700 cell data are stored in 'raw_data_SoH_protocol_expandability.zip'.

## Code overview
All of the codes used in data processing and analysis can be found in 'Fast and direct diagnosis of state of health for the spent batteries.ipynb'.

It consists of diagnostic protocol classification and SoH regression. And the prediction of 21700 cell data with feature engineering is also included.
