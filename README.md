Power Dynamics Modeling

A first-order structural abstraction framework for modern power systems and distribution networks.

Overview

This repository contains the simulation files and computational implementations of the Power Dynamics modeling framework. By operating a structural reduction from traditional second-order circuit variables—such as node voltages (V), branch currents (I), and line resistances (R)—this paradigm establishes an autonomous, first-order syntax governed exclusively by localized power variables (P) and efficiency metrics (eta).
Central to this abstraction is the formulation of the Hybrid Bus (Hbus), a virtual component with a rigorous mathematical foundation that serves as a highly scalable blueprint for mapping complex multi-terminal networks without the numerical stiffness and solver convergence failures typical of traditional circuit integration engines.
Note: The complete gnoseological and epistemological justification of this framework is addressed in a dedicated companion philosophical paper.

Key Features

• Structural Complexity Reduction: Translates conventional circuit grids into a streamlined power domain.
• Hybrid Bus (Hbus) Architecture: Implements the core virtual balancing component using a System Dynamics (SD) approach.
• High Computational Tractability: Eliminates node-voltage/branch-current algebraic loop constraints, making it ideal for fast transient analysis and real-time Digital Twins.
• Scalable Foundation: Prepared for future large-scale matrix network formulations.

Structure of the Repository

• /models: Source simulation files (e.g., AnyLogic .alp files, Python scripts).
• /scripts: Auxiliary data processing and transient verification algorithms.
• /docs: Reference documentation and manuscript preprints.

Core Mathematical Foundation

The transient behavior of the residual energy state variable inside the Hbus is governed by the following first-order Ordinary Differential Equation (ODE):
de/dt = k * (eref - e(t)) - pu(t) - pd(t)
Where:
• e(t): Instantaneous residual energy state of the node.
• pg = k * (eref - e): Proportional power injection from the generator.
• pu(t): Useful power demand used by the load.
• pd(t): Dissipated thermal power losses linked to the local efficiency.

Citation

If you use this framework or the Hbus model in your research, please cite our corresponding publications:
1. Power Dynamics and Hybrid Bus Modeling for DC Microgrids: A Structural Abstraction Approach (Technical Synthesis Paper).
2. Abstract Modeling in Renewable Power Systems: Gnoseological and Epistemological Foundations (Companion Philosophical Paper).
3. 
