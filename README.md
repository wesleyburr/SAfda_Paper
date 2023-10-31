# Modelling particle number size distribution: A continuous approach

Imputation and analysis of data for the paper entitled "Modelling particle number size distribution: A continuous approach". 

## Source Data

(some stuff from Anja)

## Imputation

The imputation of the time series (51 in total) contained in the original source data is done using the `tsinterp` package, which implements the algorithm first developed in 
[the PhD thesis](https://qspace.library.queensu.ca/server/api/core/bitstreams/bcbdd3d8-8113-4509-aabc-c8637d99ceef/content) of Wesley Burr. The code for this method is 
implemented in the [tsinterp](https://github.com/wesleyburr/tsinterp) package for R. This method uses a multi-step iterative algorithm and a Cleveland-style decomposition
of the series to produce imputed values for time series with periodic structure. The file [1_Setup_and_Impute.Rmd](https://github.com/wesleyburr/SAfda_Paper/blob/main/1_Setup_and_Impute.Rmd)
has the minimal code required to reproduce this imputation from the raw source data.

## SAfda

(some notes about the package)

## Analysis

(a guide to the analysis pathway, maybe a reference to a vignette)
