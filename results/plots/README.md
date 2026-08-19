Plots generated from XFLR5 v6.61 exported text results

Description
-----------
These PNG plots are created by `generate-plots.py` which reads the raw XFLR5 v6.61 exported text files (no data is modified or smoothed) and produces comparative visualizations.

- Data source: XFLR5 v6.61 exported `.txt` result files located under `airfoil-analysis/` and `wing-analysis/`.
- Python is used only for post-processing and visualization.

Generated plots
---------------
- `plots/airfoils/CL_vs_alpha.png` — airfoil CL vs angle of attack (deg)
- `plots/airfoils/CD_vs_alpha.png` — airfoil CD vs angle of attack (deg)
- `plots/airfoils/CL_CD_vs_alpha.png` — airfoil CL/CD vs angle of attack (deg)
- `plots/airfoils/Cm_vs_alpha.png` — airfoil Cm vs angle of attack (deg)

- `plots/wings/CL_vs_alpha.png` — wing CL vs angle of attack (deg)
- `plots/wings/CD_vs_alpha.png` — wing CD vs angle of attack (deg)
- `plots/wings/CL_CD_vs_alpha.png` — wing CL/CD vs angle of attack (deg)
- `plots/wings/Cm_vs_alpha.png` — wing Cm vs angle of attack (deg)

Notes
-----
- The script discovers files automatically and expects the repository structure to contain the airfoil and wing folders (e.g., `airfoil-analysis/CLARK Y/`).
- If files are renamed or moved, re-run the script after restoring the original structure or update the files accordingly.
- No aerodynamic data is altered — the visualizations reflect the raw numeric results exported by XFLR5.
