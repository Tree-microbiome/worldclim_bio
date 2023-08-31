# worldclim_bio
# worldclim_bio data download

install.packages("raster")
install.packages("rgdal")
rm(list = ls())
library(raster)
library(rgdal)
setwd("C:/Users/24810/Desktop/folder (2)")
w = getData('worldclim', var='bio', res=10) 
d<-read.table("sample.txt", header=T, sep="\t")
extract(w, d[c(2,3)])

