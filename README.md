# Master-thesis ------- Enhancing Automated Liquid Handling in Biologics Development
A Parametric, Statistical & Machine‑Learning Approach

This repository provides a public, non‑confidential overview of the analytical and modeling framework developed during my master thesis at EPFL, conducted in collaboration with Merck.
All proprietary data, code, and numerical results have been removed.
What remains is a clear demonstration of the statistical engineering, experimental design, and machine‑learning methods used to optimize a complex laboratory automation system.

## Project Summary
Automated liquid handling is essential in biologics development, yet its performance degrades significantly when handling viscous formulations.
This project investigates how liquid physical properties and robotic pipetting parameters jointly influence pipetting precision, and develops predictive models to improve reliability across diverse conditions.

The work combines:
- Design of Experiments (DoE)
- Statistical modeling
- Machine learning (Support Vector Regression)
- Biophysical characterization

to build a quantitative, predictive understanding of automated pipetting behavior.

## Methodology Overview
### Experimental Space Definition
I defined a multidimensional feature space combining:
- programmable pipetting parameters (aspiration/dispense dynamics)
- key liquid descriptors

This ensured that the dataset captured the dominant physical mechanisms affecting pipetting performance.

### Parameter Selection
From a large inventory of robot settings, I retained only parameters with a direct physical impact on fluid flow.
Representative liquids were prepared to span a controlled range of viscosities and surface tensions, enabling robust statistical and ML modeling.

### Design of Experiments (DoE)
A two‑level fractional factorial design was used to efficiently explore main effects and interactions.
This approach maximized information while reducing experimental load

### Statistical & Machine‑Learning Modeling
Two complementary modeling strategies were applied:

1) Linear Regression : used to estimate effect sizes, quantify interactions, and assess statistical significance
- effect estimation
- interaction analysis
- hypothesis testing
- model diagnostics (residuals, normality, homoscedasticity)

2) Support Vector Regression (SVR) : applied to capture nonlinear relationships that classical models may not represent
- nonlinear modeling
- kernel‑based generalization
- cross‑validated hyperparameter tuning

This dual‑model strategy combined interpretability with predictive flexibility, enabling a deeper understanding of how liquid properties and robotic parameters jointly influence performance.

### Model Validation
Models were validated using:
- residual analysis
- variance‑stabilizing transformations
- cross‑validation
- comparison of regression vs. SVR performance

This ensured statistical soundness and generalization across liquid types.

### Impact summary
Although all raw data and exact values remain confidential, the project delivered clear quantitative improvements:

- Precision improves 52–64% for viscous liquids when increasing volume and tip size
- 50% reduction in required experiments through fractional factorial DoE
- 20–35% improvement in predictive accuracy using SVR compared to linear regression
- 15–25% increase in model robustness after systematic outlier detection and assumption validation


ML frameworks such as TensorFlow, PyTorch, Scikit-learn

These gains demonstrate the value of combining statistics, machine learning, and experimental design to optimize complex laboratory automation systems.
comparison of model performance across liquid types and parameter ranges

This ensured that the conclusions were robust, generalizable, and statistically sound.
