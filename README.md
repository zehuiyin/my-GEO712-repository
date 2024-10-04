
<!-- README.md is generated from README.Rmd. Please edit that file -->

*This repository is an activity completed by [Zehui
Yin](https://zehuiyin.github.io/) for the course [GEOG 712 Reproducible
Research Workflow with GitHub and
R](https://academiccalendars.romcmaster.ca/preview_course.php?catoid=55&coid=274877),
taught by [Dr. Antonio Paez](https://experts.mcmaster.ca/display/paezha)
in Fall 2024.*

# Research Interest

My research interests lie in **spatial analysis**, **travel behaviour**,
**public transit**, and **shared mobility**. I am particularly
interested in using an *evidence-based approach* and *quantitative
methods*, such as *econometrics*, to examine transportation systems.
From 2022 to 2024, I worked as a research assistant in the [Suburban
Mobilities Cluster](https://www.utsc.utoronto.ca/suburban-mobilities/)
within the Department of Human Geography at the University of Toronto
Scarborough. During this time, I conducted *surveys* and *network* data
analysis to explore transportation *accessibility*, *equity*, and
*justice* in suburban areas, particularly in Scarborough, Ontario, under
the supervision of [Dr. Steven
Farber](https://www.utsc.utoronto.ca/geography/steven-farber),
[Dr. Andre Cire](https://utsc.utoronto.ca/mgmt/andre-cire), and
[Dr. Ignacio Tiznado-Aitken](https://tiznadoaitken.cl/). My works on
analyzing transport investment priorities among Scarborough residents
and cycling comfort levels on different street types in Toronto were
both funded by the [University of Toronto Excellence
Award](https://www.utsc.utoronto.ca/research/university-toronto-excellence-award).
I have also collaborated on several shared micromobility projects with
[Dr. Xiang Yan](https://www.essie.ufl.edu/people/name/xiang-yan/) from
the University of Florida. In these projects, I conducted econometric
modelling and spatial analysis to investigate the travel behaviour and
spatiotemporal patterns of shared e-scooter usage in Washington, DC, and
Los Angeles.

# Favourites

## Favourite Music

<!---
Generated using https://www.tablesgenerator.com/
--->

1.  Like the Wind (Simplified Chinese: 像风一样) by Joker Xue
    (Simplified Chinese: 薛之谦)
2.  Express Your Feelings (Simplified Chinese: 聊表心意) by Sara (Xijun)
    Liu (Simplified Chinese: 刘惜君) and Joker Xue (Simplified Chinese:
    薛之谦)
3.  The City (Simplified Chinese: 牧马城市) by Buyi Mao (Simplified
    Chinese: 毛不易)
4.  The Brightest Star in the Night Sky (Simplified Chinese:
    夜空中最亮的星) by Escape Plan (Simplified Chinese: 逃跑计划)
5.  The Final Battle (Simplified Chinese: 最后的战役) by Jay Chou
    (Simplified Chinese: 周杰伦)

## Favourite Equation

The equation below shows the OLS estimators in matrix form.

$$
\hat{\beta}=(X'X)^{-1}X'y
$$

## Favourite Artists

| Name              | Achievements              |
|-------------------|---------------------------|
| Vincent van Gogh  | The Starry Night          |
| Pablo Picasso     | Guernica                  |
| Leonardo da Vinci | Mona Lisa                 |
| Johannes Vermeer  | Girl with a Pearl Earring |
| Claude Monet      | Impression, Sunrise       |

# A Chunk of Code

``` r
# run a linear regression with the built-in dataset mtcars
m1 <- lm(mpg ~ cyl + hp + wt + vs + am, 
         data = mtcars)

# save the model results to data folder
saveRDS(m1, file = "./data/m1.rds")


# summarize the regression results
summary(m1)
#> 
#> Call:
#> lm(formula = mpg ~ cyl + hp + wt + vs + am, data = mtcars)
#> 
#> Residuals:
#>     Min      1Q  Median      3Q     Max 
#> -3.6729 -1.6583 -0.4297  1.3307  5.4688 
#> 
#> Coefficients:
#>             Estimate Std. Error t value Pr(>|t|)    
#> (Intercept) 33.24160    5.48527   6.060 2.11e-06 ***
#> cyl         -0.40179    0.79364  -0.506   0.6169    
#> hp          -0.02589    0.01387  -1.866   0.0733 .  
#> wt          -2.54332    0.93506  -2.720   0.0115 *  
#> vs           1.17067    1.81283   0.646   0.5241    
#> am           1.97575    1.64825   1.199   0.2415    
#> ---
#> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#> 
#> Residual standard error: 2.537 on 26 degrees of freedom
#> Multiple R-squared:  0.8514, Adjusted R-squared:  0.8228 
#> F-statistic:  29.8 on 5 and 26 DF,  p-value: 5.571e-10
```

# Folder Structure

<!---
Generated using https://tree.nathanfriend.io
&#10;Text used:
&#10;- data
  - ...
- data-raw
  - data_source.csv
  - ...
- images
  - toronto_crime.png
- renv
  - ...
- _dependencies.R
- my-GEO712-repository.Rproj
- README.md
- README.Rmd
- renv.lock
- ...
--->

    .
    ├── data/
    │   └── ...
    ├── data-raw/
    │   ├── data_source.csv
    │   └── ...
    ├── images/
    │   └── toronto_crime.png
    ├── renv/
    │   └── ...
    ├── _dependencies.R
    ├── my-GEO712-repository.Rproj
    ├── README.md
    ├── README.Rmd
    ├── renv.lock
    └── ...

The folder structure is illustrated in the diagram above.

- The `data/` folder stores processed data after analysis or cleaning.
- The `data-raw/` folder contains read-only raw data for the project.
  Within this folder,`data_source.csv` is a data table that includes the
  source information for all raw data, such as the download URL and the
  access date.
- The `images/` folder is designated for storing images, figures, and
  photos.
- The `_dependencies.R` file is used to add packages to the lockfile
  that are not automatically included.

# Project Data Analysis

- List the data that you expect to use, collect or create in your
  project. Identify if you are generating or collecting the data and if
  you are using existing datasets?

*I plan to compute a spatial accessibility index for transit access to
grocery stores in Hamilton at the Census Tract level, similar to the one
computed by [Statistics
Canada](https://www150.statcan.gc.ca/n1/pub/27-26-0001/272600012023001-eng.htm).
To achieve this, I will use the Hamilton Street Railway’s General
Transit Feed Specification (GTFS) data, the OpenStreetMap road network,
supermarket/grocery store locations from OpenStreetMap, and Census Tract
spatial data from Statistics Canada through [Census
Mapper](https://censusmapper.ca/api). Therefore, I will be utilizing
existing datasets.*

- Are there legal or ethical restrictions that you will need to address?

*Since I am only using open data, there are minimal legal and ethical
concerns. Open Hamilton allows me to copy, modify, publish, translate,
adapt, distribute, or otherwise use the data in any medium, mode, or
format for any lawful purpose. Similarly, OpenStreetMap grants
permission to copy, distribute, transmit, and adapt their data. Both
sources require proper credit or acknowledgment as the data providers.*

- Go through the Quick Hits for Data Management and identify possible
  strategies to build and protect the value of your data.

  - Where will you keep raw data and how will you back it up?

  *All the raw data I use will be kept in the `data-raw/` folder and
  pushed to GitHub, while also being stored locally on my laptop.
  Additionally, I’ll keep a zipped folder of all the raw data on an
  external hard drive as a physical backup.*

  - What file formats do you anticipate your data will be in? Are the
    formats open or can they be converted to open formats?

  *I anticipate my data will be in `geojson`, `csv`, `GTFS`, and `PBF`
  formats. These are all open formats, and there are open-source and
  free tools available to work with each of them.*

  - Create a File naming convention for your project data

  *I will use lowercase words and underscores for all project data,
  except for established acronyms like “GTFS,” where I will use
  capitalized characters.*

  - What standards are relevant to your project? List any existing
    standards or best practices in use in your field or in your lab?
    This could include instrument procedures or file management
    standards. What standards might you want to create to help you
    manage your data?

  *Versioning is crucial when conducting spatial analysis or econometric
  modelling. It is likely that we will try several specifications or
  different methods, resulting in multiple versions. Previously, I
  created separate folders for each version and added the date to the
  folder name. However, since we are now using Git, I will commit
  changes after every analysis step or when processed data is added to
  the project. This way, if something goes wrong, I can always revert
  back.*

  - List possible strategies you might use to document your data
    throughout your project.

  *I use a `csv` file in the `data-raw/` folder to document where and
  when I obtained each piece of raw data. Processed data will be placed
  in the `data/` folder to keep it separate from the raw data.
  Additionally, a `README` text file will be created in the data folder
  to explain any intermediate data if needed.*
