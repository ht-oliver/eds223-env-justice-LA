#### Investigation Environmental Justice in LA County in the Wake of Historical HOLC Redlining

#### Background:
*Provided by Ruth Oliver [here](https://eds-223-geospatial.github.io/assignments/HW2.html)*


Present-day environmental justice may reflect legacies of injustice in the past. The United States has a long history of racial segregation which is still visible. During the 1930’s the Home Owners’ Loan Corporation (HOLC), as part of the New Deal, rated neighborhoods based on their perceived safety for real estate investment. Their ranking system, (A (green), B (blue), C (yellow), D (red)) was then used to block access to loans for home ownership. Colloquially known as “redlining”, this practice has had widely-documented consequences not only for community wealth, but also health<sup>1</sup>. Redlined neighborhoods have less greenery<sup>2</sup> and are hotter than other neighborhoods<sup>3</sup>.

A recent study found that redlining has not only affected the environments communities are exposed to, it has also shaped our observations of biodiversity<sup>4</sup>. Community or citizen science, whereby individuals share observations of species, is generating an enormous volume of data. Ellis-Soto and co-authors found that redlined neighborhoods remain the most undersampled areas across 195 US cities. This gap is highly concerning, because conservation decisions are made based on these data.

#### Purpose:
  The purpose of this repo is to explore the lingering effects of historical redlining in LA County. 
  
  
#### Contents

```
EDS223-HW2
├── data - #empty in repository See Data Access for necessary downloads
├── eds223-env-justice-LA.Rproj
├── HW2_files
│   ├── figure-html
│   │   ├── unnamed-chunk-2-1.png
│   │   ├── unnamed-chunk-4-1.png
│   │   └── unnamed-chunk-5-1.png
│   └── libs
│       ├── bootstrap
│       │   ├── bootstrap-c0367b04c37547644fece4185067e4a7.min.css
│       │   ├── bootstrap-icons.css
│       │   ├── bootstrap-icons.woff
│       │   └── bootstrap.min.js
│       ├── clipboard
│       │   └── clipboard.min.js
│       └── quarto-html
│           ├── anchor.min.js
│           ├── popper.min.js
│           ├── quarto-syntax-highlighting-2f5df379a58b258e96c21c0638c20c03.css
│           ├── quarto.js
│           ├── tippy.css
│           └── tippy.umd.min.js
├── HW2.html
├── HW2.qmd
└── README.md
```


#### Data Access

All of the data used in this analysis has been made publicly available. The following datasets are necessary to perform this analysis. 

ejscreen - This data contains census-block level metrics for all major US cities. Data can be downloaded here: https://www.epa.gov/ejscreen/download-ejscreen-data


gdf-birds-LA - This data contains bird observation data from the city of LA. It can be downloaded here: https://www.gbif.org

mapping-inequality - This data contains historical redlining district geometries. It can be downloaded here:  https://dsl.richmond.edu/panorama/redlining/data/CA-LosAngeles

Raw data should be downloaded and placed in the 'data' folder within the repository.


#### Installations

The following is a list of R packages used in this analysis, along with brief descriptions:

| Package     | Description                                                                                                                                          |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `tidyverse` | A collection of packages for data science, including `dplyr`, `ggplot2`, `readr`, and more — useful for data wrangling, analysis, and visualization. |
| `here`      | Simplifies file paths by using a consistent project root. Helps make code more portable and easier to collaborate on.                                |
| `tmap`      | A flexible and powerful package for creating both static and interactive thematic maps.                                                              |
| `stars`     | Handles raster and spatiotemporal arrays; useful for advanced geospatial and environmental data analysis.                                            |
| `sf`        | Provides tools to work with vector spatial data (simple features) and integrates seamlessly with `ggplot2` and tidyverse workflows.                  |
| `spData`    | Offers a collection of spatial datasets for practice, demos, and testing spatial workflows.                                                          |
| `janitor`   | Tools for cleaning and inspecting data, especially helpful for fixing column names and formatting tabular outputs.                                   |
| `knitr`     | Enables dynamic report generation, embedding R code into markdown, HTML, or PDF documents.                                                           |
| `ggpubr`    | Simplifies the process of creating publication-ready plots using `ggplot2`, and supports easy arrangement of multiple plots.                         |
| `ggthemes`  | Adds additional themes, color palettes, and scales to `ggplot2` for more visually polished graphics.                                                 |


If you do not have these packages installed, you can install them in R by running the following command:

```
install.packages(c(
  "tidyverse", "here", "tmap", "stars", "sf",
  "spData", "janitor", "knitr", "ggpubr", "ggthemes"
))
```

#### Authors

Henry Oliver

#### References

<sup>1</sup> Gee, G. C. (2008). A multilevel analysis of the relationship between institutional and individual racial discrimination and health status. American journal of public health, 98(Supplement_1), S48-S56.

<sup>2</sup> Nardone, A., Rudolph, K. E., Morello-Frosch, R., & Casey, J. A. (2021). Redlines and greenspace: the relationship between historical redlining and 2010 greenspace across the United States. Environmental health perspectives, 129(1), 017006.

<sup>3</sup> Hoffman, J. S., Shandas, V., & Pendleton, N. (2020). The effects of historical housing policies on resident exposure to intra-urban heat: a study of 108 US urban areas. Climate, 8(1), 12.

<sup>4</sup> Ellis-Soto, D., Chapman, M., & Locke, D. H. (2023). Historical redlining is associated with increasing geographical disparities in bird biodiversity sampling in the United States. Nature Human Behaviour, 1-9.

<sup>5</sup> U.S. Environmental Protection Agency. Overview of Demographic Indicators in EJSCREEN. Retrieved October 18, 2025, from https://19january2017snapshot.epa.gov/ejscreen/overview-demographic-indicators-ejscreen\_.html