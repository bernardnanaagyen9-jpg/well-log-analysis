# Well log analysis: Brown A1, Russell County, Kansas

A Python workflow for basic petrophysical analysis of a single wireline log: loading, cleaning, and interpreting gamma ray, resistivity, and density curves.

## Data
- Well: Brown A 1, API 15-167-24108, Russell County, Kansas
- Source: Kansas Geological Survey (KGS) digital wireline log (LAS file)
- Depths are in feet

## Tools
Python, lasio, pandas, NumPy, Matplotlib, Jupyter (VS Code)

## Workflow
1. Load the LAS file and inspect the curves
2. Clean bad data (zero and extreme values in density, resistivity, gamma ray, caliper)
3. Define the open-hole interval from the caliper (about 2,560 to 3,320 ft)
4. Mask density where the hole is washed out
5. Calculate shale index from smoothed gamma ray
6. Calculate density porosity
7. Estimate water saturation with the Archie equation (in progress)

## Assumptions
- Limestone matrix density of 2.71 g/cc and fluid density of 1.0 g/cc
- Archie constants a = 1, m = 2, n = 2
- Density values outside the range 1.8 to 3.1 g/cc treated as bad data
- Density porosity above 30% treated as bad data
- Caliper above 9 inches treated as washout

## Limitations
- The matrix density is assumed, not measured
- No neutron or sonic log is available in this well
- Shaly rock lowers resistivity, so Archie may overestimate water saturation in those zones

## Results
To be added.

## Acknowledgements
Well data from the Kansas Geological Survey.