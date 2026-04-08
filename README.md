<h1>Master Thesis — Enhancing Automated Liquid Handling in Biologics Development</h1>
<h2>A Parametric, Statistical & Machine‑Learning Approach</h2>

<p>
  This repository provides a public, non‑confidential overview of the analytical, experimental,
  and modeling framework I developed during my master thesis at EPFL, conducted in collaboration
  with Merck. All proprietary data, code, and numerical results have been removed.
</p>

<hr/>

<h2>1. Project Summary</h2>

<p>
Automated liquid handling is essential in biologics development, yet its performance degrades
significantly when handling liquids with diverse physical properties. This project investigates how
liquid properties and robotic pipetting parameters jointly influence pipetting precision, and develops
predictive models to improve reliability across conditions.
</p>

<p>The work integrates:</p>
<ul>
  <li><strong>Robotic automation</strong></li>
  <li><strong>Laboratory formulation work</strong></li>
  <li><strong>Design of Experiments (DoE)</strong></li>
  <li><strong>Statistical modeling</strong></li>
  <li><strong>Machine learning</strong></li>
</ul>

<h3>End‑to‑End Workflow</h3>

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
|  Experimental Design   |
|  (DoE planning)        |
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
|  (Statistics + ML)     |
+-----------+------------+
            |
            v
+------------------------+
|  Insights & Guidelines |
|  robust pipetting      |
+------------------------+
</pre>

<hr/>

<h2>2. My Contributions</h2>

<p>
My work spans four major technical domains: <strong>robotic automation</strong>, <strong>laboratory formulation</strong>, 
<strong>Design of Experiments</strong>, and <strong>statistical & machine‑learning modeling</strong>.
</p>

<hr/>

<h3>2.1 Robotic Platform Work</h3>

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
  <li><strong>Configured and operated</strong> a high‑throughput automated liquid‑handling robot.</li>
  <li><strong>Tuned and validated pipetting parameters</strong> (aspiration/dispense speeds, volumes, tip types).</li>
  <li><strong>Developed structured experimental protocols</strong> for reproducibility and statistical modeling.</li>
  <li><strong>Executed systematic test campaigns</strong> across multiple liquid types and parameter combinations.</li>
  <li><strong>Diagnosed and mitigated robotic failure modes</strong> such as dripping or incomplete aspiration.</li>
</ul>

<hr/>

<h3>2.2 Laboratory Preparation of Solutions</h3>

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
  <li><strong>Prepared controlled liquid formulations</strong> spanning a wide range of physical properties.</li>
  <li><strong>Adjusted compositions</strong> to isolate the effect of specific biophysical properties.</li>
  <li><strong>Performed biophysical measurements</strong> to generate high‑quality model inputs.</li>
  <li><strong>Ensured reproducibility</strong> through standardized preparation and documentation workflows.</li>
</ul>

<hr/>

<h3>2.3 Design of Experiments (DoE)</h3>

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

<ul>
  <li><strong>Designed and executed a fractional factorial DoE</strong> to explore main effects and interactions efficiently.</li>
  <li><strong>Mapped DoE conditions to robotic protocols</strong> to ensure reproducible execution.</li>
  <li><strong>Reduced experimental load by 50%</strong> while maximizing information content.</li>
  <li><strong>Generated statistically balanced datasets</strong> for downstream modeling.</li>
</ul>

<hr/>

<h3>2.4 Statistical & Machine‑Learning Modeling</h3>

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
</pre>

<ul>
  <li><strong>Built linear regression models</strong> for effect estimation and interaction analysis.</li>
  <li><strong>Implemented Support Vector Regression (SVR)</strong> to capture nonlinear relationships.</li>
  <li><strong>Performed cross‑validation and hyperparameter tuning</strong> for robust generalization.</li>
  <li><strong>Compared model performance</strong> across liquid types and parameter ranges.</li>
  <li><strong>Used ML frameworks</strong> such as Scikit‑learn (and compatible workflows with TensorFlow/PyTorch).</li>
</ul>

<hr/>

<h2>3. Methodology</h2>

<h3>3.1 Experimental Space Definition</h3>
<p>
I defined a multidimensional feature space combining:
</p>
<ul>
  <li><strong>Programmable pipetting parameters</strong> (aspiration/dispense dynamics, volumes, tip sizes)</li>
  <li><strong>Liquid descriptors</strong> (viscosity, surface tension, etc.)</li>
</ul>

<h3>3.2 Parameter Selection</h3>
<p>
From a large inventory of robot settings, I retained only parameters with a direct physical
impact on fluid flow. Representative liquids were prepared to span a controlled range of
properties, enabling robust statistical and ML modeling.
</p>

<h3>3.3 DoE Execution</h3>
<p>
A two‑level fractional factorial design was used to efficiently explore main effects and
interactions while reducing experimental load.
</p>

<hr/>

<h2>4. Impact Summary</h2>

<ul>
  <li><strong>52–64% improvement in precision</strong> for viscous liquids when increasing volume and tip size.</li>
  <li><strong>50% reduction in required experiments</strong> through fractional factorial DoE.</li>
  <li><strong>20–35% improvement in predictive accuracy</strong> using SVR compared to linear regression.</li>
  <li><strong>15–25% increase in model robustness</strong> after systematic outlier detection and assumption validation.</li>
</ul>

<p>
These gains demonstrate the value of combining robotic optimization, careful laboratory preparation,
statistical design, and modern machine‑learning techniques to improve automated liquid handling in
biologics development.
</p>
