
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Sex health clinics in Toronto

<!-- badges: start -->
<!-- badges: end -->

This repository holds information about sex health clinics in Toronto.
It supports a student project for ENVSOCTY 4GA3 (Applied Spatial
Statistics) by:

- Victoria Baginski  
- Eva Boomsma  
- Peri Juskiw
- Samantha Kirtz  
- Chantelle Lobo  
- Helena Muirhead-Hunt  
- Eva Novoselac  
- Audreana Rossi

The students have collected information about clinics in Toronto, and
have the Dissemination Areas (DAs). They shared the DA centroids and the
location of the clinics.

I obtained the road network in Toronto from
[BBBike](https://download.bbbike.org/osm/bbbike/Toronto), and use
{[r5r](https://ipeagit.github.io/r5r/index.html)} to calculate driving
times from DA centroids to each clinic.

The file with the road network is not shared on GitHub (it is a large
file), so if you wish to replicate the routing calculations you need to
obtain a copy and place in folder `data-raw/r5_graph/`. The file must be
in `osm.pbf` format, which is what {r5r} uses.

The notebook with the routing is in folder
`data-raw\01-OSM-Network-and-Routing`. You can check it for details.

The following data objects are available:

- `data/clinics.rda`: a simple features table with the location of the
  clinics.  
- `data/da_centroids.rda`: a simple features table with the centroids of
  the Dissemination Areas (DAs) in Toronto.
- `data/ttm_driva_da.rda`: a simple features table with Toronto’s
  Dissemination Areas (DAs) and population statistics by various age
  groups.  
- `data/ttm_driva_da.rda`: a data frame with driving times from DA
  centroid to clinic. The travel time is in minutes.
