# Chicago Active Employee Project

A comprehensive data analysis project examining the Chicago Active Employee dataset with advanced gender detection, clustering analysis, and predictive modeling.

## Features

- **Enhanced Gender Detection**: Uses comprehensive name lists for improved gender classification
- **Exploratory Data Analysis**: Statistical summaries and visualizations
- **K-Means Clustering**: Employee segmentation based on salary and gender
- **Machine Learning Models**: 
  - Gender prediction using job characteristics
  - High earner classification with 90%+ accuracy

## Project Structure

```
chicago-active-employee-project/
├── notebook.ipynb          # Main analysis notebook (refactored)
├── requirements.txt        # Python dependencies
├── .gitignore             # Git ignore rules
├── README.md              # This file
├── venv/                  # Virtual environment
└── data/                  # Data files (created during analysis)
```

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd chicago-active-employee-project
```

### 2. Create and Activate Virtual Environment
```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
# On Linux/Mac:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook notebook.ipynb
```

## Data Source

The project analyzes the Chicago Active Employee dataset, which is automatically downloaded from:
- **Source**: [City of Chicago Data Portal](https://data.cityofchicago.org/)
- **Dataset**: [Current Employee Names, Salaries, and Position Titles](https://data.cityofchicago.org/Administration-Finance/Current-Employee-Names-Salaries-and-Position-Titles/xzkq-xp2w)
- **Direct Link**: https://data.cityofchicago.org/Administration-Finance/Current-Employee-Names-Salaries-and-Position-Titles/xzkq-xp2w
- **Format**: Excel (.xlsx)
- **Update Frequency**: Updated quarterly
- **License**: Public Domain

## Key Analysis Sections

1. **Data Loading & Preprocessing**
   - Automated data loading and cleaning
   - Column normalization and missing value handling

2. **Gender Detection Enhancement** 
   - Custom name-based gender classification
   - Uses comprehensive male/female/neutral name lists

3. **Exploratory Data Analysis**
   - Gender and employment distribution analysis
   - Salary analysis across departments and job types
   - Statistical summaries and visualizations

4. **Feature Engineering & Clustering**
   - K-means clustering with optimal K selection
   - Employee segmentation analysis
   - Cluster characteristic evaluation

5. **Machine Learning Models**
   - Gender prediction model (multinomial classification)
   - High earner prediction model (binary classification)
   - Model evaluation with ROC curves and confusion matrices

## Key Findings

- **Workforce Composition**: Clear gender imbalance in municipal workforce
- **Salary Patterns**: Strong correlation between departments, job titles, and compensation
- **Predictive Accuracy**: High earner prediction achieves >90% accuracy
- **Data Quality**: Successfully processed ~30,857 employee records

## Technical Stack

- **Python 3.12+**
- **Data Processing**: pandas, numpy
- **Visualization**: matplotlib, seaborn  
- **Machine Learning**: scikit-learn
- **File Handling**: openpyxl
- **Gender Detection**: gender-guesser + custom name lists
- **Development**: jupyter, black, flake8, pytest

## Usage

After setup, simply run the notebook cells in order. The analysis will:

1. Download the latest Chicago employee data
2. Process and clean the dataset
3. Generate comprehensive visualizations
4. Perform clustering analysis
5. Train and evaluate ML models
6. Save processed data as `chicago_dataset_cleaned.csv`

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Data License
The Chicago employee data is publicly available through the City of Chicago Data Portal under the Public Domain license.

