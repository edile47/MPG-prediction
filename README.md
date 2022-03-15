# STAT306 Group Project

### Setting up R for use with Jupyter Lab
[Install Miniconda](https://docs.conda.io/en/latest/miniconda.html)
[Install R](https://www.r-project.org/)

Create a conda environment to run Jupyter Lab from by typing the following in a terminal:

```
conda create --name r_jupyter jupyter lab
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

### Research Question

Can fuel efficiency be predicted by knowing the design specifications of a vehicle? Which design variables most significantly affect fuel efficiency?

