# CovidPPI
Analytical workflow used in "Chronic Acid Suppression and Social Determinants of COVID-19 Infection" and sample data

## Generating Sample Data
1). Example [sample data](/CensusData/SampleData.xlsx) is already available in the [CensusData](/CensusData/) directory. If you wish to directly use this data, you can skip this section and move to the next section. <br>
2). To generate your own sample data or see how we generated the example [sample data](/CensusData/SampleData.xlsx), please use the script [GenerateSampleData.Rmd](/GenerateSampleData.Rmd). <br> <br>
Required R packages are:
- [tidyverse](https://cran.r-project.org/web/packages/tidyverse/index.html)
- [openxlsx](https://cran.r-project.org/web/packages/openxlsx/index.html)
<br>
Make sure to change to working directory: <br>

```pathUse <- "/Users/douglasarneson/Documents/ButteLab/CovidPPIstudyVivek/FirstStudy/Analysis/DougResultsV1"```

## Running Analytical Pipeline
1). Make sure you have the sample data (either the example [sample data](/CensusData/SampleData.xlsx) or generate using the provided script [GenerateSampleData.Rmd](/GenerateSampleData.Rmd) ).

2). Install required R packages:
- [tidyverse](https://cran.r-project.org/web/packages/tidyverse/index.html)
- [table1](https://cran.r-project.org/web/packages/table1/index.html)
- [DataExplorer](https://boxuancui.github.io/DataExplorer/)
- [tidycensus](https://cran.r-project.org/web/packages/tidycensus/index.html)
- [mice](https://cran.r-project.org/web/packages/mice/index.html)
- [tibbletime](https://cran.r-project.org/web/packages/tibbletime/index.html)

3). Get required publicly available geocoded social determinants of health and mobility datasets from our [figshare repository](https://figshare.com/articles/dataset/Datasets_supporting_analytical_workflow_of_Chronic_Acid_Suppression_and_Social_Determinants_of_COVID-19_Infection/13380356).
- zcta_county_rel_10.txt - Population and housing density from the 2010 decennial census
- cre-2018-a11.csv - Community Resilience Estimates which is is the capacity of individuals and households to absorb, endure, and recover from the health, social, and economic impacts of a disaster such as a hurricane or pandemic
- zcta_tract_rel_10.txt - Relationship between ZCTA and US Census tracts (used to map census tracts to ZCTA)
- mask-use-by-county.txt - Mask Use By County comes from a large number of interviews conducted online by the global data and survey firm Dynata at the request of The New York Times. The firm asked a question about mask use to obtain 250,000 survey responses between July 2 and July 14
- mobility_report_US.txt - Google mobility report which charts movement trends over time by geography, across different categories of places such as retail and recreation, groceries and pharmacies, parks, transit stations, workplaces, and residential
- ACS2015_zctaallvars.csv - Social Deprivation Index is a composite measure of area level deprivation based on seven demographic characteristics collected in the American Community Survey (https://www.census.gov/programs-surveys/acs/) and used to quantify the socio-economic variation in health outcomes

4). Put the files downloaded from our [figshare repository] and either the example [sample data](/CensusData/SampleData.xlsx) or data generated using the provided script [GenerateSampleData.Rmd](/GenerateSampleData.Rmd) into a directory called <b>CensusData</b> which is inside of your working directory.

5). Get a US Census API key from: https://api.census.gov/data/key_signup.html

6). Replace "YourKeyHere" text with the obtained census API key:

``` censusAPIkey <- "YourKeyHere" ```
