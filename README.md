<h1>Master Thesis — Enhancing Automated Liquid Handling in Biologics Development</h1>
<h2>A Parametric, Statistical & Machine‑Learning Approach</h2>

<p>
  This repository provides a public, non‑confidential overview of the analytical, experimental,
  and modeling framework I developed during my master thesis at EPFL, conducted in collaboration
  with Merck. All proprietary data, code, and numerical results have been removed.
</p>

<p>
  What remains is a clear demonstration of my contributions across:
</p>
<ul>
  <li><strong>Robotic automation</strong> — configuration, operation, and optimization of a liquid‑handling platform</li>
  <li><strong>Laboratory formulation work</strong> — preparation and characterization of controlled liquid solutions</li>
  <li><strong>Statistical engineering</strong> — experimental design, regression modeling, and inference</li>
  <li><strong>Machine learning</strong> — nonlinear modeling and predictive performance optimization</li>
</ul>

<hr />

<h2>Project Summary</h2>
<p>
  Automated liquid handling is essential in biologics development, yet its performance degrades
  significantly when handling formulations with different physical liquid properties. This project investigates
  how liquid physical properties and robotic pipetting parameters jointly influence pipetting
  precision, and develops predictive models to improve reliability across diverse conditions.
</p>

<p>
  The work integrates:
</p>
<ul>
  <li><strong>Design of Experiments (DoE)</strong></li>
  <li><strong>Statistical modeling</strong> (linear regression, interaction analysis)</li>
  <li><strong>Machine learning</strong> (Support Vector Regression)</li>
  <li><strong>Biophysical characterization</strong> of liquid properties</li>
</ul>

<p>
  to build a quantitative, predictive understanding of automated pipetting behavior.
</p>

<hr />

<h2>My Contributions</h2>

<h3>Robotic Platform work</h3>

<pre>
+-----------------------------+
|  Define Pipetting Goals     |
|  (volume, liquid type, etc.)|
+--------------+--------------+
               |
               v
+-----------------------------+
|  Select Robot Parameters    |
|  - aspiration speed         |
|  - dispense speed           |
|  - tip type / volume        |
+--------------+--------------+
               |
               v
+-----------------------------+
|  Program / Configure Robot  |
+--------------+--------------+
               |
               v
+-----------------------------+
|  Execute Pipetting Runs     |
+--------------+--------------+
               |
               v
+-----------------------------+
|  Monitor Behavior & Issues  |
|  (drips, air intake, etc.)  |
+--------------+--------------+
               |
               v
+-----------------------------+
|  Refine Parameters          |
|  (iterative optimization)   |
+-----------------------------+
</pre>


<ul>
  <li><strong>Configured and operated</strong> a high‑throughput automated liquid‑handling robot used in biologics development.</li>
  <li><strong>Selected, tuned, and validated pipetting parameters</strong> such as aspiration/dispense speeds, volumes, tip types.</li>
  <li><strong>Developed structured experimental protocols</strong> to ensure reproducibility and compatibility with statistical modeling.</li>
  <li><strong>Implemented systematic test campaigns</strong> across multiple liquid types and parameter combinations.</li>
  <li><strong>Diagnosed and mitigated robotic failure modes</strong> (e.g., dripping, incomplete aspiration, air intake) through parameter optimization.</li>
</ul>

<h3>Laboratory preparation of solutions</h3>

<pre>
+-------------------------------+
|  Define Target Property Space |
|  (viscosity, surface tension) |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Design Formulation Set       |
|  (low / medium / high ranges) |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Prepare Solutions in Lab     |
|  (standardized protocols)     |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Measure Properties           |
|  (viscosity, σ, etc.)         |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Validate & Document          |
|  (reproducibility, logging)   |
+-------------------------------+
</pre>


<ul>
  <li><strong>Prepared controlled liquid formulations</strong> spanning a wide range of liquid physical prooperties</li>
  <li><strong>Adjusted compositions</strong> to isolate the effect of specific biophysical properties on pipetting performance.</li>
  <li><strong>Performed biophysical measurements</strong> to generate high‑quality input features for modeling.</li>
  <li><strong>Ensured formulation reproducibility</strong> through standardized preparation and documentation workflows.</li>
</ul>

<h3>Statistical & Machine‑Learning modeling</h3>
<ul>
  <li><strong>Designed the experimental plan</strong> using fractional factorial DoE to efficiently explore main effects and interactions.</li>
  <li><strong>Built linear regression models</strong> to quantify effect sizes, interactions, and statistical significance.</li>
  <li><strong>Implemented Support Vector Regression (SVR)</strong> to capture nonlinear relationships between liquid properties and robotic parameters.</li>
  <li><strong>Performed cross‑validation and hyperparameter tuning</strong> to ensure robust generalization.</li>
  <li><strong>Compared model performance</strong> across liquid types, parameter ranges, and modeling approaches.</li>
  <li><strong>Used ML frameworks</strong> such as Scikit‑learn (and compatible workflows with TensorFlow/PyTorch).</li>
</ul>

<hr />

<h2>Methodology Overview</h2>

<pre>
+------------------------+
|  Robotic Platform      |
|  setup & tuning        |
+-----------+------------+
            |
            v
+------------------------+
|  Lab preparation       |
|  controlled liquids    |
+-----------+------------+
            |
            v
+------------------------+
|  Automated experiments |
|  pipetting on robot    |
+-----------+------------+
            |
            v
+------------------------+
|  Data Collection       |
|  volumes, errors, etc. |
+-----------+------------+
            |
            v
+------------------------+
|  Modeling & Analysis   |
|  (Statisticss + ML)    |
+-----------+------------+
            |
            v
+------------------------+
|  Insights & Guidelines |
|  robust pipetting      |
+------------------------+
</pre>


<h3>Experimental space definition</h3>
<p>
  I defined a multidimensional feature space combining:
</p>
<ul>
  <li><strong>Programmable pipetting parameters</strong> (aspiration/dispense dynamics, volumes, tip sizes)</li>
  <li><strong>Liquid descriptors</strong> </li>
</ul>
<p>
  This ensured that the dataset captured the dominant physical mechanisms affecting pipetting
  performance.
</p>

<h3>Parameter selection</h3>
<p>
  From a large inventory of robot settings, I retained only parameters with a direct physical
  impact on fluid flow. Representative liquids were prepared to span a controlled range of
  physical liquid properties, enabling robust statistical and ML modeling.
</p>

<h3>Design of Experiments (DoE)</h3>

<pre>
+-------------------------------+
|  Identify Factors & Ranges    |
|  - robot parameters           |
|  - liquid properties          |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Build DoE Plan               |
|  (fractional factorial)       |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Map DoE Runs to Robot        |
|  (parameter sets per run)     |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Execute Runs on Robot        |
|  (automated pipetting)        |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Record Outputs               |
|  (precision, errors, etc.)    |
+-------------------------------+
</pre>

<p>
  A two‑level fractional factorial design was used to efficiently explore main effects and
  interactions while reducing experimental load.
</p>

<h3>Statistical & Machine‑Learning modeling</h3>

<pre>
+-------------------------------+
|  Raw Experimental Data        |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Data Cleaning                |
|  - outlier detection          |
|  - consistency checks         |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Feature Engineering          |
|  - transforms (e.g. log)      |
|  - derived features           |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Statistical Modeling         |
|  - linear regression          |
|  - effect & interaction       |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Machine Learning (SVR)       |
|  - nonlinear modeling         |
|  - CV + hyperparameter tuning |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Model Comparison & Validation|
|  (metrics, residuals, etc.)   |
+---------------+---------------+
                |
                v
+-------------------------------+
|  Final Insights & Guidelines  |
+-------------------------------+
</pre>


<h4>1) Linear Regression</h4>
<ul>
  <li>Effect estimation</li>
  <li>Interaction analysis</li>
  <li>Hypothesis testing</li>
  <li>Model diagnostics (residuals, normality, homoscedasticity)</li>
</ul>

<h4>2) Support Vector Regression (SVR)</h4>
<ul>
  <li>Nonlinear modeling</li>
  <li>Kernel‑based generalization</li>
  <li>Cross‑validated hyperparameter tuning</li>
</ul>

<p>
  This dual‑model strategy combined interpretability with predictive flexibility.
</p>

<h3>Model Validation</h3>
<ul>
  <li>Residual analysis</li>
  <li>Variance‑stabilizing transformations</li>
  <li>Cross‑validation</li>
  <li>Comparison of regression vs. SVR performance</li>
</ul>

<hr />

<h2>Impact Summary</h2>
<p>
  Although all raw data and exact values remain confidential, the project delivered clear
  quantitative improvements:
</p>
<ul>
  <li><strong>52–64% improvement in precision</strong> for viscous liquids when increasing volume and tip size.</li>
  <li><strong>50% reduction in required experiments</strong> through fractional factorial DoE.</li>
  <li><strong>20–35% improvement in predictive accuracy</strong> using SVR compared to linear regression.</li>
  <li><strong>15–25% increase in model robustness</strong> after systematic outlier detection and assumption validation.</li>
</ul>

<p>
  These gains demonstrate the value of combining:
</p>
<ul>
  <li><strong>Hands‑on robotic platform optimization</strong></li>
  <li><strong>Careful laboratory preparation and characterization of solutions</strong></li>
  <li><strong>Statistical design and analysis</strong></li>
  <li><strong>Modern machine‑learning techniques</strong></li>
</ul>

<p>
  to optimize complex laboratory automation systems in biologics development.
</p>
