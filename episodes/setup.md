[Go to main page](../README.md)

# Information for the workshop 

During the workshop we will provide access to virtual machines will all packages and software preinstalled. These will only during the workshop.


# For after the workshop

If you like to continue after the workshop, you'll need to setup the following software and libraries into your own computer.

## Download R and R Studio
1. Go to the [CRAN website](https://cran.r-project.org) and follow the instructions to download and install R.
2. Download and install [RStudio](https://www.rstudio.com/products/rstudio/download/#download).

## Installing additional packages
Open RStudio and install the following packages.

```{r}
## To install needed CRAN packages:
install.packages("tidyverse")
install.packages("GGally")
install.packages("caret")
install.packages("gmodels")
install.packages("rpart")
install.packages("rpart.plot")
install.packages("dendextend")
install.packages("randomForest")
install.packages("mlr3")
install.packages("devtools")
install.packages("klaR")
install.packages("kernlab")
install.packages("ggbiplot")

## To install needed Bioconductor packages:
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install()
BiocManager::install(c("limma", "edgeR"))

```


In case you encounter issues with `ggbiplot`, please have a look at this [GitHub issue](https://github.com/vqv/ggbiplot/issues/53#issuecomment-456464102).

Load them to make sure they were successfully installed.
```
# Load packages
library(ggbiplot)

library(tidyverse) # working with data frames, plotting
library(GGally)
library(caret)
library(gmodels)
library(rpart)
library(rpart.plot)
library(randomForest)

library(dendextend)
library(mlr3)


library(edgeR)      # cpm, etc -- RNA-Seq normalization
library(limma)      # lmFit, etc -- fitting many models
```
