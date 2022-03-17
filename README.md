# STAT306 Group Project

## Data Source
[Combined Cycle Power Plant Data Set](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant). The dataset contains 9568 data points collected from a Combined Cycle Power Plant over 6 years (2006-2011), when the power plant was set to work with full load.

## Setting up R for use with Jupyter Lab
[Install Miniconda](https://docs.conda.io/en/latest/miniconda.html)
[Install R](https://www.r-project.org/)

Create a conda environment to run Jupyter Lab from by typing the following in a terminal:

```
conda create --name r_jupyter jupyterlab
```

Then activate the environment by typing `conda activate r_jupyter`

With R installed locally, type `R` in a terminal to open the R interactive interpreter. Then type the following:

```
install.packages("devtools")
devtools::install_github("IRkernel/IRkernel")
system.file('kernelspec', package = 'IRkernel')
```

The final line will output a directory path similar to `/Library/Frameworks/R.framework/Versions/4.1-arm64/Resources/library/IRkernel/kernelspec`. Copy the path and quit the R interpreter by typeing `q()`. In the terminal you activated the `r_jupyter` conda environment in, type:

```
jupyter kernelspec install <you-path-from-previous-step> --name 'R' --user
```

Using the path to your kernels spec. After the kernel has been added to jupyter lab, type `jupyter lab` in the same terminal, and you will be able to use the **R** kernel with a Jupyter notebook.

## Research Question

Can we predict the net-full-load power output of Combined Cycle Power Plants in Turkey by knowing the realtaive humidity (percent), air temperature (C&deg), air pressure (milibar), and exhaust vacuum pressure (cm Hg)?

