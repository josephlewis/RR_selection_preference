# A data-driven framework for inferring selection preferences from archaeological routes

This repository contains all the data and scripts required to fully reproduce all analyses presented in the paper "_A data-driven framework for inferring selection preferences from archaeological routes_" authored by **Lewis**, J

Getting Started
---------------

1. Open project using RR_selection_preference.Rproj to ensure relative paths work.
2. Run the _000_Main.R_ R script in the R folder to load the necessary libraries

**Code**
   * _001_Preprocess_dem.R_ preprocesses the Digital Elevation Model (DEM) used in the analysis.
   * _002_preprocess_routes.R_ preprocesses the Roman roads used in the analysis
   * _003_preprocess_movement_steps.R_ preprocesses the Roman roads for the step-selection analysis
   * _004_fit_model.R_ fits model using inlabru
   * _005_model_plots_fe.R_ calculates the typical (global) selection strength of slope gradient for Roman roads in Britain

   * _006_model_plots_re.R_ calculates the selection strength of slope gradient for individual Roman roads in Britain

   * _007_model_plots_re2.R_ plots selection strengths of each individual Roman road and produces example of step-selection analysis results
   
**Data**
1. Roman_roads 
  * _engineered_roman_roads.geojson_ - Roman roads in Britain. Digital Britannia. Digitised by Haken (2026). https://roadsofromanbritain.org/digital-britannia/overview.html
  * _military_installations.geojson_ - Roman military installations. Digital Britannia. Digitised by Haken (2026). https://roadsofromanbritain.org/digital-britannia/overview.html
  * _military_installations2.gpkg/.rds - Subset of Roman military installations. Digital Britannia. Digitised by Haken (2026). https://roadsofromanbritain.org/digital-britannia/overview.html
  * _RR.gpkg/.rds_ - Roman roads in Britain used in the analysis. Subset of Roman roads in Britain. Digital Britannia. Digitised by Haken (2026). https://roadsofromanbritain.org/digital-britannia/overview.html
2. DEM
  * _DEM_modifed.tif_ - Digital Elevation Model of Britain. Subset from the 30 metre Digital Terrain Model for Continental Europe. https://doi.org/10.5281/ZENODO.4724549

**Output**
1. _Figures_
2. 
  * _M1.rds_ - Step-selection analysis model. See _004_fit_model.R_
  * _movement_factors.rds_ - preprocessesed Roman roads for the step-selection analysis. See _003_preprocess_movement_steps.R_
  * _movement_factors_strata_count.rds_ - Summary of preprocessesed Roman roads for the step-selection analysis
  * _RR_selection.gpkg/.rds - Individual Roman roads with selection strengths
  * _samples_long_fixed.rds._ / _samples_long_specific.rds._ - Summary of selection strengths for specific slope gradients


License
---------------
CC-BY 3.0 unless otherwise stated (e.g. see License for Hengl (2020), https://doi.org/10.5281/ZENODO.4724549). 

Session Info
---------------
R version 4.6.1 (2026-06-24)
Platform: x86_64-pc-linux-gnu
Running under: Linux Mint 22.3

Matrix products: default
BLAS:   /usr/lib/x86_64-linux-gnu/blas/libblas.so.3.12.0 
LAPACK: /usr/lib/x86_64-linux-gnu/lapack/liblapack.so.3.12.0  LAPACK version 3.12.0

locale:
 [1] LC_CTYPE=en_GB.UTF-8       LC_NUMERIC=C               LC_TIME=en_GB.UTF-8        LC_COLLATE=en_GB.UTF-8     LC_MONETARY=en_GB.UTF-8    LC_MESSAGES=en_GB.UTF-8   
 [7] LC_PAPER=en_GB.UTF-8       LC_NAME=C                  LC_ADDRESS=C               LC_TELEPHONE=C             LC_MEASUREMENT=en_GB.UTF-8 LC_IDENTIFICATION=C       

time zone: Europe/London
tzcode source: system (glibc)

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] patchwork_1.3.2   ggrepel_0.9.8     ggthemes_5.2.0    ggdist_3.3.3      ggsflabel_0.0.1   tidyterra_1.2.0   ggplot2_4.0.3     inlabru_2.15.0    INLA_26.02.06    
[10] Matrix_1.7-6      data.table_1.18.4 stringr_1.6.0     tidyr_1.3.2       dplyr_1.2.1       tidygraph_1.3.1   sfnetworks_0.6.6  geosphere_1.6-8   sf_1.1-2         
[19] terra_1.9-34     

loaded via a namespace (and not attached):
 [1] gtable_0.3.6           spatstat.sparse_3.2-0  lattice_0.23-1         vctrs_0.7.3            tools_4.6.1            spatstat.utils_3.2-4   generics_0.1.4        
 [8] goftest_1.2-3          tibble_3.3.1           proxy_0.4-29           pkgconfig_2.0.3        sfheaders_0.4.5        KernSmooth_2.23-27     RColorBrewer_1.1-3    
[15] S7_0.2.2               distributional_0.8.1   lifecycle_1.0.5        compiler_4.6.1         farver_2.1.2           deldir_2.0-4           fmesher_0.8.0         
[22] spatstat.linnet_3.5-3  codetools_0.2-20       spatstat.explore_3.8-2 class_7.3-24           pillar_1.11.1          crayon_1.5.3           classInt_0.4-11       
[29] spatstat.model_3.7-2   lwgeom_0.2-17          spatstat.univar_3.2-0  rpart_4.1.27           abind_1.4-8            nlme_3.1-171           spatstat.geom_3.8-2   
[36] tidyselect_1.2.1       stringi_1.8.7          purrr_1.2.2            splines_4.6.1          polyclip_1.10-7        grid_4.6.1             cli_3.6.6             
[43] magrittr_2.0.5         e1071_1.7-17           spatstat.data_3.1-9    withr_3.0.3            tensor_1.5.1           scales_1.4.0           igraph_2.3.3          
[50] otel_0.2.0             mgcv_1.9-4             rlang_1.3.0            Rcpp_1.1.2             spatstat.random_3.5-1  glue_1.8.1             DBI_1.3.0             
[57] rstudioapi_0.19.0      R6_2.6.1               units_1.0-1
