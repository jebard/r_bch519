# Input and output controls

In the fundamentals section, we covered setting up your project data folder. If everything is loaded into your directory structure properly, we should be able to easily use 
relative paths to quickly load up data files.


## Loading from a flat file
In the first case, we will load up a .csv format file to start. R has several built in tools to read flat files.

```r
# read in the data input file labelled SEPA-2023-Metadata.csv
# we are going to assign metadata variable with the information.
# I personally like to be explicit and set the column separator every time, as well as tell R to use the first row in the file as column headers. 
metadata <- read.csv(file="data/SEPA-2023-Metadata.csv", sep=",", header=T)

# quickly check that the table read in properly
head(metadata)
View(metadata)

```

## Saving data out from a variable into a flat file
Now that we have the data from metadata saved into a variable, we can easily export it into a new file to illustrate saving data.

```r
# using the metadata above, lets export
write.csv(file="output/data.write.test.csv", metadata)
```

## Loading and Saving RData objects
We can also load and  save variables out into R Data objects. This is especially beneficial for complex data objects that aren't simpley flat files. This is
very common for example in single-cell sequencing, where we have many samples, many cells, and many processing steps required during the analysis. 

```r
# Save an RDS format file out
saveRDS(file="output/metadata.rds",metadata)

# load an RDS format file
reloaded_metadata <- readRDS(file="output/metadata.rds")
```


