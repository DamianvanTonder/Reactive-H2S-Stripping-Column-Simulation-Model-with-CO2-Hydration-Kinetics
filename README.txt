# _Reactive H₂S Stripping Column Model with CO₂ Hydration Kinetics_
A comprehensive Python-based simulation tool for modeling reactive hydrogen sulfide stripping columns with explicit incorporation of carbon dioxide hydration kinetics. This software addresses critical limitations in traditional equilibrium-based models by accounting for the slow kinetics of CO₂ hydration, providing accurate predictions for industrial process design and optimization.

## _Project Overview_
This project develops a stage-wise computational model for a reactive H₂S stripping column that converts sodium hydrosulfide (NaHS) into sodium bicarbonate (NaHCO₃) using carbon dioxide as the stripping agent. The key innovation lies in incorporating the kinetic limitations of CO₂ hydration to carbonic acid - a rate-limiting step that is typically neglected in equilibrium-based simulations but critically affects real-world performance.

### _Industrial Context_
- Application: Conversion of low-value sodium sulfate (Na₂SO₄) waste into high-value sodium carbonate (Na₂CO₃)
- Process: Multi-step pathway involving reactive stripping of H₂S from aqueous NaHS solutions
- End Products: Sodium bicarbonate (intermediate) → Sodium carbonate (final product for glass manufacturing, paper industry)

## _Key Features_
### _Core Modeling Capabilities_
- Kinetic-Enhanced Modeling: Explicit incorporation of CO₂ hydration kinetics (k<sub>f</sub> = 0.030259 s⁻¹)
- Stage-wise Simulation: Sequential solution from top to bottom with counter-current flow
- Multi-component Chemistry: Simultaneous tracking of 8 aqueous species and 3 gas components
- Comprehensive Equilibria: Integration of multiple acid-base equilibria and gas-liquid phase equilibria
- Temperature-Dependent Properties: Dynamic calculation of Henry's constants, dissociation constants, and transport properties

### _Advanced Analysis Tools_
- Automated Sensitivity Analysis: Six comprehensive parameter studies
- Process Optimization: Identification of optimal operating conditions
- Design Correlations: Automatic generation of empirical design equations
- Validation Tools: Residual analysis and convergence diagnostics
- Visualization Suite: Comprehensive plotting of concentration profiles, pH distribution, and performance metrics

### _Numerical Robustness_
- Enhanced Stability: Variable scaling and multiple initial guess strategies
- High Precision: Convergence criteria of 10⁻¹² for accurate mass balance closure
- Stiff System Handling: Special techniques for managing wide concentration ranges
- Error Handling: Comprehensive try-catch blocks and solution validation

## _Scientific Innovation_
### _Problem Addressed_
Traditional equilibrium-based models assume instantaneous CO₂ hydration, leading to significant prediction errors:

- Underestimation of required column stages at high recovery targets
- Inaccurate pH profiles affecting species distribution calculations
- Poor prediction of gas-phase compositions and flow rates
- Unreliable scaling from laboratory to industrial applications

### _Solution Approach_
This software explicitly models the kinetic limitation through:

- Rate Expression: First-order kinetics for CO₂ + H₂O ⇌ H₂CO₃
- Temperature Dependence: Arrhenius-type correlation for rate constant
- Mass Balance Integration: Kinetic rate terms in material balances
- Equilibrium Coupling: Simultaneous solution of fast equilibria and slow kinetics

### _Key Findings_
- Critical Discovery: Kinetic effects become dominant at recovery targets >97%
- Optimal Conditions: 20°C temperature, 2.8 atm pressure minimize stage requirements
- Design Impact: Traditional models can underestimate equipment size by 40-60%
- pH Management: Kinetic limitations significantly affect acid-base chemistry

## _Simulation Capabilities_
### _Base Case Performance_
Operating Conditions:
- Temperature: 25°C
- Pressure: 1 atm
- Liquid Feed: 1 L/s, 0.8 mol/L NaHS
- Gas Feed: 0.9 mol/s CO₂
- Target H₂S Recovery: 99.99%

Results:
- Required Stages: 63
- Total Column Volume: 11,340 L
- Final pH: 7.35
- CO₂ Excess Required: 12.5%

### _Sensitivity Analysis Range_
- Temperature: 15-47°C (optimal at 20°C, 62 stages minimum)
- Pressure: 0.3-5 atm (optimal at 2.8 atm, 38 stages minimum)
- Stage Volume: 50-550 L (trade-off between residence time and capital cost)
- Gas Flowrate: 0.825-0.9 mol/s (higher flows reduce stages but increase operating costs)
- Feed Concentration: 0.5-0.87 mol/L (higher concentrations dramatically increase complexity)
- Recovery Target: 97-99.999% (diminishing returns above 99%)

## _Prerequisites_
- Python ≥ 3.8
- numpy ≥ 1.20.0
- scipy ≥ 1.7.0
- pandas ≥ 1.3.0
- matplotlib ≥ 3.3.0

## _Validation & Accuracy_
### _Numerical Validation_
- Mass Balance Closure: Residuals < 10⁻¹²
- Charge Balance Accuracy: Electroneutrality maintained within 10⁻¹⁰
- Convergence Rate: 95%+ success rate across parameter ranges
- Stability Testing: Robust performance with extreme operating conditions

### _Physical Constraint Validation_
- pH Range: Realistic values (6.5-8.5) maintained throughout
- Species Concentrations: All positive, physically meaningful values
- Phase Equilibrium: Henry's law consistency verified
- Energy Balance: Temperature effects properly captured

### _Benchmark Comparisons_
- Equilibrium Models: 15-40% deviation at high recovery targets
- Literature Data: Good agreement with experimental CO₂ hydration rates
- Industrial Data: Consistent with reported column performance where available

## _Applications & Impact_
### _Process Design Applications_
- Column Sizing: Accurate prediction of stage requirements and dimensions
- Operating Optimization: Identification of cost-optimal conditions
- Retrofit Analysis: Evaluation of existing column performance
- Scale-up Guidance: Reliable transition from pilot to industrial scale

### _Research Applications_
- Kinetic Studies: Investigation of reaction rate limitations in multiphase systems
- Model Development: Framework for other reactive separation processes
- Process Intensification: Identification of bottlenecks and improvement opportunities
- Environmental Impact: Waste valorization and sustainable processing

### _Commercial Impact_
- Cost Reduction: Avoid over-design through accurate modeling
- Risk Mitigation: Reliable performance predictions reduce project risks
- New Business Models: Enable economic evaluation of waste-to-value processes
- Technology Transfer: Support industrial implementation of research developments

## _Future Development_
### _Planned Enhancements_
- Non-isothermal Models: Temperature variation along column height
- Multi-component Extensions: Additional ionic species and reactions
- Dynamic Simulation: Transient behavior and control system design
- Process Integration: Heat exchanger networks and energy optimization
- Machine Learning: AI-enhanced parameter estimation and optimization

### _Research Opportunities_
- Experimental Validation: Systematic comparison with pilot plant data
- Catalyst Integration: Enhanced CO₂ hydration kinetics through catalysis
- Alternative Configurations: Packed columns, reactive distillation variants
- Process Synthesis: Integration with upstream and downstream operations

## _Documentation & Support_
### _Documentation Structure_
- User Guide: Step-by-step tutorials and examples
- API Reference: Detailed function and class documentation
- Theory Manual: Mathematical derivations and modeling assumptions
- Validation Report: Comprehensive accuracy and reliability studies

### _Getting Help_
- GitHub Issues: Bug reports and feature requests
- Discussions: Community forum for questions and collaboration
- Email Support: damianvantonder111@gmail.com
- Academic Collaboration: Open to research partnerships

## _Citation_
If you use this software in your research, please cite:
- @software{vantonder2024reactive,
  title={Reactive H₂S Stripping Column Model with CO₂ Hydration Kinetics},
  author={van Tonder, D.A.},
  year={2025},
  url={https://github.com/DamianvanTonder/Reactive-H2S-Stripping-Column-Simulation-Model-with-CO2-Hydration-Kinetics.git},
  version={2.0}
}

## _License_
This project is licensed under the MIT License - see the LICENSE file for details.
- [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)

## _Acknowledgments_
- Prof. DS van Vuuren (University of Pretoria) - Project supervision
- Mr. Gontse Mokonyane - Experimental data contribution in the previous year (2024)
- Chemical Engineering Department, University of Pretoria - Research support

## _Contact_
- Damian A. van Tonder
- Email: u21449300@tuks.co.za or damianvantonder111@gmail.com
- LinkedIn: https://www.linkedin.com/in/damian-van-tonder-69b198272/
- ORCID: 0009-0008-8364-3736
