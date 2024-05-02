# genome-annotation-multivisual

This allows for the visualization of any coding regions coming from the protein alignments. support for the visualization of all the coding regions for a specific ids. implemented dplyr so that it will be faster.

- run the function as 
```
genecoding <- function(genomealigned, ids, strand)
 # where genomealigned is the gff file 
 # ids your specific ids
 # strand specific strand positive or negative
 output <- genecoding(multi.gff, "ids", positive)
```
- plot the genes as 
```
library(ggplot2)
library(gggenes)
ggplot(output, aes(xmin = start, xmax = end, y = molecule, fill = gene)) +
  geom_gene_arrow() +
  facet_wrap(~ molecule, scales = "free", ncol = 1) +
  scale_fill_brewer(palette = "Set3")
```
Gaurav \
Academic Staff Member \
Bioinformatics \
Institute for Biochemistry and Biology \
University of Potsdam \
Potsdam,Germany


