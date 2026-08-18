# Airfoil Comparison Results

## 1. Overview

Five airfoils were compared using XFLR5 based on maximum lift, aerodynamic efficiency, endurance-related performance, and pitching moment.

The analysed profiles were:

* S1210 (12%)
* E214 (11.1%)
* NACA 4412
* Clark Y
* MH32 (8.7%)

## 2. Comparative Results

| Airfoil         |     Max CL | α at Max CL |   Max CL/CD | α at Max CL/CD | Max CL^1.5/CD | α at Max Endurance |      Cm |
| --------------- | ---------: | ----------: | ----------: | -------------: | ------------: | -----------------: | ------: |
| **S1210 (12%)** | **2.0313** |       15.0° |     59.2979 |           8.5° |   **81.3765** |               8.5° | -0.2214 |
| E214 (11.1%)    |     1.4089 |       13.5° | **62.0238** |           7.5° |       70.7860 |               7.5° | -0.1163 |
| NACA 4412       |     1.4471 |       15.0° |     55.0542 |           8.5° |       64.0422 |               9.5° | -0.0750 |
| Clark Y         |     1.3704 |       12.5° |     53.0832 |           7.0° |       57.3744 |               8.5° | -0.0648 |
| MH32 (8.7%)     |     1.1351 |        9.5° |     53.9551 |           5.5° |       50.7174 |               6.0° | -0.0492 |

Source: XFLR5 airfoil analysis results.

## 3. Interpretation

### Maximum Lift

S1210 achieved the highest maximum lift coefficient:

**CL,max = 2.0313**

The next highest value was NACA 4412 at 1.4471.

This makes S1210 the strongest candidate according to the maximum-lift criterion within the analysed conditions.

### Aerodynamic Efficiency

E214 achieved the highest maximum lift-to-drag ratio:

**CL/CD = 62.0238 at α = 7.5°**

S1210 achieved:

**CL/CD = 59.2979 at α = 8.5°**

Therefore, E214 was the most efficient airfoil according to the maximum CL/CD criterion.

### Endurance-Related Performance

The `CL^1.5/CD` criterion was used as an endurance-related metric in the original analysis.

S1210 achieved the highest value:

**CL^1.5/CD = 81.3765 at α = 8.5°**

E214 was second at 70.7860.

### Pitching Moment

The pitching moment coefficient at the maximum-endurance condition was also considered.

S1210 had a value of:

**Cm = -0.2214**

The negative pitching moment indicates a nose-down pitching tendency under the analysed condition.

## 4. Overall Selection

S1210 was selected as the overall candidate based on the combined priority given to:

1. Maximum lift capability
2. Endurance-related performance
3. Aerodynamic efficiency
4. Pitching behaviour

However, S1210 was **not the best performer in every individual metric**.

E214 achieved the highest maximum `CL/CD`, making it the strongest candidate when aerodynamic efficiency alone is prioritised.

Therefore:

> **S1210 is the overall selected candidate under the defined performance priorities, while E214 provides the highest aerodynamic efficiency according to maximum CL/CD.**

## 5. Important Note

These results represent XFLR5 numerical predictions under the specified analysis conditions. They should not be interpreted as experimental validation.

The values are dependent on the selected Reynolds number, transition settings, angle-of-attack range, and XFLR5 aerodynamic model.

## 6. Wing-Level Analysis

Separate wing-level analyses were performed for the same five airfoils using XFLR5.

The wing results are stored in:

```text
wing-analysis/
├── CLARKY/
├── E214/
├── MH32/
├── NACA4412/
└── S1210/
```

The original `.xfl` project files and `.txt` output files are retained for each configuration.

For example, the S1210 wing analysis used a freestream velocity of **12 m/s** and evaluated angles of attack from **-5° to 15° in 0.5° increments** using VLM1.
