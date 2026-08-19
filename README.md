# XFLR5 Airfoil & Wing Analysis Project

Comparative aerodynamic analysis of five airfoils and their corresponding wing configurations using XFLR5.

## Overview

This project investigates the aerodynamic characteristics of five airfoil profiles and evaluates their performance using XFLR5.

The airfoils analysed are:

* Clark Y
* E214
* MH32
* NACA 4412
* S1210

Both **2D airfoil analyses** and **3D wing analyses** were performed to compare aerodynamic behaviour and identify a suitable airfoil based on lift, aerodynamic efficiency, and endurance-related performance criteria.

## Objectives

* Compare the aerodynamic performance of different airfoil profiles.
* Evaluate lift and drag characteristics across a range of angles of attack.
* Compare maximum lift coefficient and lift-to-drag ratio.
* Evaluate an endurance-related aerodynamic criterion.
* Extend the analysis from individual airfoils to finite-wing configurations.
* Select an overall candidate based on the defined performance criteria.

## Software

* **XFLR5 v6.61**
* Analysis methods include viscous airfoil analysis and Vortex Lattice Method (VLM) wing analysis.

## Airfoil Analysis

The airfoil analyses were performed at:

| Parameter       |                    Value |
| --------------- | -----------------------: |
| Reynolds number |                  100,000 |
| Mach number     |                        0 |
| Ncrit           |                        9 |
| Transition      |   100% top / 100% bottom |
| Angle of attack | Approximately -5° to 15° |

The original XFLR5 project files (`.xfl`) and exported result files (`.txt`) are included in the repository.

## Wing Analysis

The corresponding wing configurations were analysed using XFLR5 VLM.

For the S1210 wing analysis, for example, the analysis was performed at a freestream velocity of **12 m/s**, with angles of attack ranging from **-5° to 15° in 0.5° increments**.

The original XFLR5 project and result files are provided for reproducibility.

## Comparative Results

The following results were obtained from the airfoil comparison:

| Airfoil         |     Max CL | α at Max CL |   Max CL/CD | α at Max CL/CD | Max CL^1.5/CD | α at Max Endurance |
| --------------- | ---------: | ----------: | ----------: | -------------: | ------------: | -----------------: |
| **S1210 (12%)** | **2.0313** |       15.0° |     59.2979 |           8.5° |   **81.3765** |               8.5° |
| E214 (11.1%)    |     1.4089 |       13.5° | **62.0238** |           7.5° |       70.7860 |               7.5° |
| NACA 4412       |     1.4471 |       15.0° |     55.0542 |           8.5° |       64.0422 |               9.5° |
| Clark Y         |     1.3704 |       12.5° |     53.0832 |           7.0° |       57.3744 |               8.5° |
| MH32 (8.7%)     |     1.1351 |        9.5° |     53.9551 |           5.5° |       50.7174 |               6.0° |

## Performance Criteria

The main criteria used for comparison were:

### Maximum Lift Coefficient, CL

Represents the maximum lift capability obtained in the analysed range of angle of attack.

### Maximum Lift-to-Drag Ratio, CL/CD

Represents aerodynamic efficiency. A higher value indicates a more favourable lift-to-drag relationship.

### CL^1.5/CD

Used as an endurance-related performance criterion in the analysis.

### Pitching Moment Coefficient, Cm

Used to examine the pitching tendency of the airfoil.

## Results & Interpretation

S1210 produced the highest maximum lift coefficient among the five analysed airfoils and also produced the highest value of the endurance-related `CL^1.5/CD` criterion.

E214 produced the highest maximum `CL/CD`, indicating that it achieved the highest aerodynamic efficiency according to that particular criterion.

Therefore, the selection of S1210 as the overall candidate is based on the combined priority given to **lift capability and endurance-related performance**, rather than claiming that it is superior in every individual metric.

## Python Post-Processing

Python was used in VS Code for automated post-processing and visualization of the aerodynamic data exported from XFLR5.

The Python scripts were used to:

- Import and process XFLR5 polar data.
- Generate comparative **CL–α, CD–α, CL/CD–α, and Cm–α** plots.
- Compare the aerodynamic performance of the selected airfoils.
- Automatically generate plots for analysis and presentation.

## Conclusion

Based on the defined selection criteria, **S1210 was selected as the overall candidate** among the five analysed airfoils.

However, the results also show that airfoil selection depends on the performance objective. E214 demonstrated a higher maximum lift-to-drag ratio, while S1210 demonstrated substantially higher maximum lift and the highest endurance-related criterion within the analysed data.

The wing-level XFLR5 analyses are included to extend the comparison beyond isolated 2D airfoil behaviour and examine the corresponding finite-wing configurations.

## Repository Structure

```text
XFLR5-Airfoil-Wing-Analysis-Project/
│
├── airfoil-analysis/
│   ├── CLARKY/
│   ├── E214/
│   ├── MH32/
│   ├── NACA4412/
│   └── S1210/
│
├── wing-analysis/
│   ├── CLARKY/
│   ├── E214/
│   ├── MH32/
│   ├── NACA4412/
│   └── S1210/
│
├── README.md
└── LICENSE
```

Each analysis directory contains the original XFLR5 project file and corresponding exported results.

## Limitations

The results in this repository are numerical XFLR5 predictions and should not be interpreted as experimental validation.

In particular, the wing analyses and airfoil analyses use different aerodynamic modelling approaches, so their coefficients should not be directly treated as equivalent datasets.

Further work could include mesh/convergence studies, experimental validation, additional Reynolds numbers, and comparison with higher-fidelity aerodynamic methods.

## Author

**Monish**

Aerospace Engineering Student, 
R.V. College of Engineering, Bengaluru
