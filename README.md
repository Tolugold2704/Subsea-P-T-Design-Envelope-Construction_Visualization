#EXERCISE 1: Subsea-P-T-Design-Envelope-Construction_Visualization
OCEON Module 2 - Case Exercise 1: Subsea P-T Design Envelope for Flow Assurance. Implements pressure_temperature_envelope() with full validation, 2D visualization of safe operating region bounded by hydrate dissociation, WAT crystallization, MAOP/ADP limits with 6 jumpers,3D P-T-Flow envelope, and operational compliance % calculator.

#EXERCISE 2:Case Exercise 2: Corrosion Rate Prediction and Remaining Life
#### Overview
Implements a physics-based corrosion prediction and asset integrity workflow to forecast remaining useful life (RUL) of subsea jumpers using synthetic SCADA data.
#### What This Code Does
**Task 1 - Corrosion Model Engine:**
`de_Waard_Milliams()` corrosion rate model with full unit tests. Calculates CO2 corrosion rate from temperature, CO2 partial pressure, pH, and flow parameters with validation.
**Task 2 - Synthetic SCADA Generation:**
Generates a realistic 10-year synthetic SCADA dataset (hourly readings) for the Usan field. Parameter ranges: Temperature, Pressure, CO2 mole %, pH, flow velocity calibrated to field conditions. Output: `usan_field_synthetic_scada_2016_2026.csv`
**Task 3 - Physics Feature Pipeline:**
Applies `PhysicsFeaturePipeline` to the synthetic data to enrich raw SCADA with physics-informed features and computes monthly average corrosion rates.
**Task 4 - RUL & Risk Classification:**
Calculates Remaining Useful Life for each of the 6 jumpers from the case study. Produces RUL vs. Corrosion Rate visualization with colour-coded risk classification(Low / Medium / High / Critical).
