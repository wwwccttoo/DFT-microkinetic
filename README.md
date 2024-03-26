# DFT-Microkinetic Modelling for Plasma Catalysis

Please view our full paper in the JACS Au (https://pubs.acs.org/doi/full/10.1021/jacsau.3c00654)

If you find this repository or our work helpful, please cite as:
``` bibtex
@article{shao2024study,
  title={A Study on the Role of Electric Field in Low-Temperature Plasma Catalytic Ammonia Synthesis via Integrated Density Functional Theory and Microkinetic Modeling},
  author={Shao, Ketong and Mesbah, Ali},
  journal={JACS Au},
  volume={4},
  number={2},
  pages={525--544},
  year={2024},
  publisher={ACS Publications}
}
```

## Dependencies
In addition to the normal packages such as numpy, scipy and matplotlib, the analysis of this work requires on the following packages:

* `qtplaskin` **!Critical!** Please following the instruction below
* `ase` required for atomistic simulation analysis
* `SALib` required for sobol sensitibity analysis
* `ax-platform` required for multi-objective Bayesian optimization
* `seaborn` required for plotting

### qtplaskin
The package you may find that its online version may not working. We provide a corrected version in this repository. To install it, please following the README in the qtplaskin folder.

## ZDPlasKin Compilation
Both the DFT-microkinetic and microkinetic models are developed using ZDPlasKin. Additional, the DFT-microkinetic model is adapted based on the codes provided by Dr. Jungmi Hong and Dr. Anthony Bruce Murphy. If you consider any further usage and/or adaption of these models, please also cite the following paper
``` bibtex
@article{hong2017kinetic,
  title={Kinetic modelling of NH3 production in N2--H2 non-equilibrium atmospheric-pressure plasma catalysis},
  author={Hong, Jungmi and Pancheshnyi, Sergey and Tam, Eugene and Lowke, John J and Prawer, Steven and Murphy, Anthony B},
  journal={Journal of Physics D: Applied Physics},
  volume={50},
  number={15},
  pages={154005},
  year={2017},
  publisher={IOP Publishing}
}
```

For ZDPlasKin code compilation, please refer to http://www.zdplaskin.laplace.univ-tlse.fr/zdplaskin-solver/index.html, according to your operation system.

## Data
To reproduce the figures showed in the paper, we have provided all the necessary data files.
### Parameter Reflection Analysis
This correlates to the first part of the results section in the paper. Necessary data files are
* `base_0.06_350.pkl`
* `base_0.06_550.pkl`
* `base_0.11_350.pkl`
* `base_0.11_550.pkl`
* `extract_0.06_350.pkl`
* `extract_0.06_550.pkl`
* `extract_0.11_350.pkl`
* `extract_0.11_550.pkl`

**base** refers to the microkinetic model results under the varying electric field and temperature conditions.\
**extract** refers to the DFT-microkinetic model results under the varying electric field and temperature conditions.

### Sobol Sentivity Analysis
This correlates to the second part of the results section in the paper. Necessary files are
* `./sobol_res/total_res_base`
* `./sobol_res/total_res_extract`
**base** refers to the microkinetic model sobol results.\
**extract** refers to the DFT-microkinetic model sobol results.
***Note***: To reproduce the figure, making sure your SALib version is `1.3.12`.

### Multi-objective Bayesian Optimization
This correlates to the second part of the results section in the paper. This analysis is only done on the DFT-microkinetic model. Thus, the only required file to reproduce the results is `485run.csv`.

## Rights and Collaborators
(c) 2024 Mesbah Lab

in collaboration with Ali Mesbah.

Questions regarding this code may be directed to ketong_shao (at) berkeley.edu
