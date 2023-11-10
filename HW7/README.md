**kidpack: kidney microarray data**
https://www.bioconductor.org/packages/release/data/experiment/manuals/kidpack/man/kidpack.pdf

Microarrays are a technology used to measure the expression levels of thousands of genes simultaneously.
Data from microarray experiments is often represented as a table with rows corresponding to genes and columns corresponding to different samples (e.g., different tissues, time points, or experimental conditions).
The values in the table represent the measured expression levels of each gene in each sample. These values can be raw intensity values or normalized values.

RNA sequencing (RNA-seq) is a more recent and versatile technology for gene expression profiling. It provides a digital measurement of RNA abundance.
RNA-seq data is typically stored in a format called FASTQ, which contains the raw sequence data. After processing, the data can be represented as a table similar to microarray data.
The table includes rows for genes and columns for samples, with values representing the expression levels. The units may be counts (number of reads mapped to a gene) or normalized values, such as fragments per kilobase of transcript per million mapped reads (FPKM) or transcripts per million (TPM).

Kidney microarray data: There were three different subtypes of renal cell cancer (RCC): clear cell (cc), papillary (p),
and chromophobe (ch). These pheno-variables may be used for classification or differential
expression. The gene expression is quite strongly associated with the subtype.

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC187526/
<img width="759" alt="Screen Shot 2023-11-09 at 10 29 32 PM" src="https://github.com/fedhere/DSPS_FBianco/assets/1696902/1b544051-54ab-4a92-9337-ac8c6711b07b">

_An underlying assumption is that by clustering genes based on similarity of their expression patterns in a limited set of experiments, we can establish guilt by association—that is, genes with similar expression patterns are more likely to have similar biological function_

_It is easy to construct examples in which genes known to share similar functions end up in different clusters [...] 
However, as long as clustering by expression pattern is used as a means to group by putative biological function, it is meaningful to ask which method performs best. 
With this goal in mind, how might we compare two clustering results derived from the same expression data set? 
Different clustering results might be obtained from different clustering algorithms, or from different choices within a clustering algorithm. 
The latter choices might include algorithm parameters (e.g., number of clusters), the method of calculating distance between two gene expression vectors (e.g., Euclidean or Pearson correlation), 
or different ways of preprocessing data (e.g., the log transformation)._

_For most methods of clustering, the user must specify the number of clusters, and often quickly wonders, 
“What is the true number of clusters?” Many data-centric techniques have been applied to this problem, with conclusions based on which number of clusters achieves the best balance of data point dispersion within and between clusters, but none has proven robust across diverse data types (Everitt 1980). 
[...] it seems likely that there is no single true number of clusters for gene expression data. We should perhaps ask, “What choice of cluster number would be most useful?”_

_**When the objective of clustering is to bring genes of similar function together, we assert that the best method of clustering a particular data set is that which has the strongest tendency to bring genes of similar function together
[...]. With this in mind, we should instead ask, “What choice of number of clusters generally yields the most information about gene function (where function is known)?” 
For other clustering choices, we might ask, “Which distance measure generally yields the most information about gene function (where function is known)?”**_
