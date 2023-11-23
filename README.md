# Modelling particle number size distribution: A continuous approach

Imputation and analysis of data for the paper entitled "Modelling particle number size distribution: A continuous approach". The data files are too large for GitHub, so are located on [Zenodo](https://zenodo.org/uploads/10201840).

## Source Data

(some stuff from Anja)

## Imputation

The imputation of the time series (51 in total) contained in the original source data is done using the `tsinterp` [package](https://github.com/wesleyburr/tsinterp), which implements the algorithm first developed in 
[the PhD thesis](https://qspace.library.queensu.ca/server/api/core/bitstreams/bcbdd3d8-8113-4509-aabc-c8637d99ceef/content) of Wesley Burr. This method uses a multi-step iterative algorithm and a Cleveland-style decomposition
of the series to produce imputed values for time series with periodic structure. The file [1_Setup_and_Impute.Rmd](https://github.com/wesleyburr/SAfda_Paper/blob/main/1_Setup_and_Impute.Rmd)
has the minimal code required to reproduce this imputation from the raw source data.

## SAfda

The [SAfda](https://github.com/I-MH/SAfda) package contains the core routines required to estimate the FDA bases and other utility routines. This allows the estimation of source apportionment through these continuous functional bases,
and all of the analysis provided in these routines. 

## Analysis

... this will eventually be a full vignette ...

We start in [2_Process_Compute.Rmd](https://github.com/wesleyburr/SAfda_Paper/blob/main/2_Process_Compute.Rmd), where we initialize the parameters and establish 
the basis functions needed for the rest of the analysis. The central core of this file contains two chunks which collectively can take many hours to run
(although they have been parallelized, so on a sufficiently powerful system, they can run in under an hour). The outputs of these chunks has been
saved and is available on the Zenodo repository (above, first section). 
