# Biodiversity in national parks

Portfolio data analysis project exploring species observations and conservation status across U.S. national parks.

## Project summary

This project analyzes biodiversity records from the National Parks Service to understand how conservation status varies across species classes and parks. The analysis is performed in a Jupyter Notebook and supported by reusable utility functions in a small Python package.

Primary workflow:
1. Load and inspect raw species and observation data.
2. Clean and standardize fields (including conservation labels and park names).
3. Merge datasets for cross-park and cross-class analysis.
4. Build summary tables and statistical comparisons.
5. Produce visualizations for conservation status and observation distributions.

## Reasearch focus

Core questions addressed in the notebook include:
- What is the distribution of listed vs not-listed species by class?
- How does conservation status vary by species class?
- How do listed species and observations differ across parks?
- Which parks and categories show the strongest concentration of listed or at-risk species?

## Dataset

Raw files are in `data/raw/`:
- `species_info.csv`
- `observations.csv`

Fields used in analysis:
- `species_info.csv`: category, scientific_name, common_names, conservation_status
- `observations.csv`: scientific_name, park_name, observations

## Project structure

```text
Biodiversity in national parks/
├── assets/
│   ├── css/
│   ├── images/
│   └── links/
├── cfg/
│   ├── matplotlib.yaml
│   ├── pandas.yaml
│   └── statistics.yaml
├── data/
│   └── raw/
│       ├── observations.csv
│       └── species_info.csv
├── ntb/
│   ├── Biodiversity in national parks.ipynb
│   └── Example solution.ipynb
├── plots/
├── src/
│   └── binp/
│       ├── __init__.py
│       ├── display_data.py
│       ├── utils.py
│       └── visualization.py
├── pyproject.toml
├── poetry.lock
└── LICENSE
```

## Tech stack

- Python 3.11-3.12
- pandas
- numpy
- scipy
- matplotlib
- seaborn
- pyyaml
- Jupyter Notebook / IPython
- Poetry for dependency and environment management

## Setup

### 1) Clone and enter the project

```bash
git clone <your-repo-url>
cd "Biodiversity in national parks"
```

### 2) Install dependencies

```bash
poetry install
```

### 3) Start the notebook

```bash
poetry run jupyter notebook
```

Open:
- `ntb/Biodiversity in national parks.ipynb`

## Running the analysis

Inside the notebook:
1. Run setup/import/configuration cells.
2. Load data from `./data/raw/`.
3. Execute cleaning and transformation steps.
4. Run visualization and hypothesis-test sections.
5. Review exported figures in `plots/`.

## Example outputs

The project already includes many generated figures in `plots/`, such as:
- `Species counts over conservation status.svg`
- `Conservation status vs. park distribution.svg`
- `Boxplot of class observations.png`
- `Birds distribution between parks.svg`
- `Warbler distribution over parks.svg`

## Key takeaways

From the current notebook outputs:
- Most species are not listed, with listed species concentrated in specific classes.
- Conservation-status composition differs by class.
- Observation patterns vary across parks, with Yellowstone often showing high counts in plotted summaries.
- Species-level and class-level comparisons highlight useful priorities for conservation reporting.

## Reproducibility notes

- All dependencies are pinned in `pyproject.toml` and `poetry.lock`.
- Configuration files under `cfg/` control display/statistics/plot defaults.
- Utility functions in `src/binp/` support repeated data-display and transformation tasks.

## License

This project is licensed under the MIT License. See `LICENSE` for details.
