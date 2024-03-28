# Installing Packages in R
Packages are basic extension of R that provide additional functions to do some analysis. For example, the popular "ggplot2" library
has been widely adopted to produce a huge array of different types of graphs and plots using common syntax. While most R installations
may come pre-loaded with ggplot2, installing the newest version of ggplot2 is good practice.

## Installing from CRAN
CRAN is the primary respository for R packages. To install a package using CRAN, first identify the package you want to install.
Next, we can quickly execute the install command using the following syntax:

```R
# Basic installation function for CRAN
install.packages()
install.packages("ggplot2") # installs a specific package to your system
```

## Installing from Bioconductor
For Bioinformatics, Bioconductor is a popular resource for packages as well. It is also managed by a team of programmers at Roswell Park!

To install using bioconductor (assuming you have the bioconductor package installed from CRAN first).
``` R
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("DESeq2")
``` 

## Load a package into your system
Assuming your installations all worked, which ~50% of the time it does without issue, the next step is to load the specific for use.
This is similiar to the import statements in python (import biopython).

``` R
library(ggplot2) # loads ggplot2 package
library(DEseq2) # loads the DESeq2 package
```

Lastly, to check to see which packages are currently loaded in your R enviornment, you can issue the sessionInfo() function.

``` R
sessionInfo()
```






