# Grouped Feature Importance and Combined Features Dependence Plot

This repository gives access to an implementation of the methods
presented in the paper submission “Grouped Feature Importance and Combined Features Dependence Plot”, 
as well as all code that was used for the
simulations and the usecase.

This repository is structured as follows:

``` 
    ├── code/                     # All code               
    |   ├── functions/            # Implemented functions
    |   ├── simulations/          # Scripts for simulation examples in paper
    |   |   ├── analysis/         # Scripts used to create figures and tables in the paper for simulation examples
    |   |   ├── experiments/      # Scripts used to create data for simulation examples
    |   ├── usecase/              # Scripts used to create data, figures and tables in usecase section
    ├── results/                  # Location where all data and figures are stored
    │   ├── figures/              # Location where final figures for paper are stored
    │   ├── simulation_results/   # Location where all data of simulation examples is stored
    │   ├── usecase_results/      # Location where all usecase data is stored
    ├── LICENSE
    └── README.md               
```



## Reproduce Experiments


Steps to reproduce the experiments of the simulation experiments.

1.  Install all required packages.

<!-- end list -->

``` r
# from CRAN
install.packages(c("ranger", "dplyr", "batchtools", "mlr", "ggplot2", "gridExtra", "tidyr", "reshape2",
"ggExtra", "future.apply", "BBmisc", "data.table", "stringi", "checkmate", "kernlab", "xtable", "mlrCPO", "devtools"))

# from github
devtools::install_github("giuseppec/featureImportance")
install_github("nickseedorff/totalvis")
```

2.  Create an experimental registry, add experiments and problem and run simulations via
    scripts in subfolder `code/simulations/experiments`. Data produced by the scripts is stored in 
    the subfolder `results/simulation_results` as a separate registry.

3.  To reproduce figures and tables of Section 3 and 4, run the scripts in subfolder `code/simulations/analysis`. The scripts are names with respect to the references subsections in the paper. Figures produced within the script are stored in `results/figures` 
    the subfolder `results/simulation_results` as a separate registry.    