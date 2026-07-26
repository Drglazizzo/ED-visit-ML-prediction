```python
# README.md content - Copy this into a code cell and run to create the file

readme_content = """# ED Visit ML Prediction

## Overview
Machine learning models for predicting Emergency Department outcomes using the MC-MED dataset. This repository contains the complete code implementation for my thesis research.

## Models Implemented
- **XGBoost** (GPU accelerated)
- **LightGBM** (GPU accelerated)
- **Random Forest**
- **TabNet** (Deep Learning)

## Prediction Tasks
1. **ED-LOS ≥ 8 hours** - Prolonged emergency department stay
2. **Hospital Admission** - Binary admission prediction
3. **Hosp-LOS > 7 days** - Prolonged hospital stay (admitted patients only)

## Features
- **29 admission-available clinical predictors**
- Demographics, triage vitals, chief complaints, comorbidity burden, home medications
- Chronological train/val/test splits (no data leakage)
- Class imbalance handling with scale-positive weighting

## Key Results
| Model | ED-LOS AUC | Admission AUC | Hosp-LOS AUC |
|-------|------------|---------------|--------------|
| Random Forest | **0.660** | **0.812** | **0.702** |
| XGBoost | 0.659 | 0.816 | 0.701 |
| LightGBM | 0.648 | 0.817 | 0.689 |
| TabNet | 0.639 | 0.815 | 0.689 |

## SHAP Analysis
Complete interpretability for ALL models including:
- Bar plots (feature importance)
- Summary (bee swarm) plots
- Waterfall plots
- Force plots
- Dependence plots (top 5 features)

## Repository Structure
```
ED-visit-ML-prediction/
├── Public_Health.ipynb    # Main Jupyter notebook with complete implementation
├── README.md              # This file
└── .gitignore             # Excluded files and folders
```

## Installation
```bash
# Clone repository
git clone https://github.com/Drglazizzo/ED-visit-ML-prediction.git

# Install dependencies
pip install pandas numpy scikit-learn xgboost lightgbm pytorch-tabnet shap matplotlib seaborn torch
```

## Usage
1. Set data path in the notebook:
```python
DATA_PATH = r"D:\Thesis\Data"
OUTPUT_PATH = r"E:\TSINGHUA\thisis\Paper\output_paper"
```
2. Run notebook cells sequentially
3. Outputs saved to `output_paper/` folder

## Requirements
- Python >= 3.8
- CUDA-capable GPU recommended for XGBoost and TabNet

## Author
**ONYEDIKACHI IKENNA ONWURAH**
- Email: drglazcode@outlook.com
- GitHub: [@Drglazizzo](https://github.com/Drglazizzo)

## License
MIT License

## Citation
```bibtex
@mastersthesis{onwurah2024mlhealth,
  author = {Onwurah, Onyedikachi Ikenna},
  title = {Machine Learning for Predicting Emergency Department Outcomes},
  school = {Tsinghua University},
  year = {2025}
}
```
"""

# Write README.md file
with open('README.md', 'w', encoding='utf-8') as f:
    f.write(readme_content)

print("✅ README.md created successfully!")
print("\nFile contents preview:")
print("-" * 50)
print(readme_content[:500] + "...")
print("-" * 50)
print("\n📁 File location:", os.path.abspath('README.md'))
```

After running this cell, you can add and commit the README file:

```bash
git add README.md
git commit -m "Add README.md"
git push
```
