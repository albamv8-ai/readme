# Biomolecular Mass Quantization

## Overview

This repository contains the analysis code and datasets for the study:
**"Quantized Mass Scaling in Biomolecules via the Fine-Structure Constant and Geometric-Eulerian Foundations"**

## Model

The molecular mass of biomolecules follows a discrete geometric progression:

**M = L₀ · (e^(25α))^q**

Where:
- **L₀ = 75.03 Da** (glycine molecular weight)
- **α = 0.0072973525693** (fine-structure constant)
- **q ∈ ℤ** (integer quantum number)
- **25 = (2√2)² + (2√2)² + (√3)⁴** (Eulerian geometric identity)

## Results

- **Dataset**: 218 biomolecules (proteins, nucleic acids, lipids, carbohydrates)
- **R²**: 0.9993
- **Mean error**: 4.31%
- **P-value**: < 0.001

## Files

### Scripts
- `main_analysis.py`: Main analysis and error calculation
- `plotting.py`: Generate publication-quality figures
- `monte_carlo.py`: Monte Carlo simulation for P-value calculation
- `validation.py`: Comprehensive statistical validation

### Data
- `protein_quantization_results.csv`: Results for 120 proteins
- `validation_results.csv`: Statistical validation results
- `monte_carlo_results.csv`: Monte Carlo simulation results

### Figures
- `fig1_model_error_vs_mass.png`: Error vs. molecular mass
- `fig2_error_distribution.png`: Error distribution histogram
- `fig3_error_by_category.png`: Error by protein size category

## Requirements

- Python 3.7+
- NumPy
- Pandas
- SciPy
- Matplotlib

## Usage

```bash
# Run main analysis
python main_analysis.py

# Generate figures
python plotting.py

# Run Monte Carlo validation
python monte_carlo.py

# Run comprehensive validation
python validation.py