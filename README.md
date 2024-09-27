
<!-- README.md is generated from README.Rmd. Please edit that file -->

*This repository is an activity for the course [GEOG 712 Reproducible
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
lm(mpg ~ cyl + hp + wt + vs + am,
   data = mtcars) |>
  # summarize the regression results
  summary()
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
  - Transit_Service_Areas.geojson
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
    │   └── Transit_Service_Areas.geojson
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
