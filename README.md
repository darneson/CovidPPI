# CovidPPI
Analytical workflow used in "Chronic Acid Suppression and Social Determinants of COVID-19 Infection" and sample data

## Generating Sample Data
1). Example [sample data](/CensusData/SampleData.xlsx) is already available in the [CensusData](/CensusData/) directory. If you wish to directly use this data, you can skip this section and move to the next section. <br>
2). To generate your own sample data or see how we generated the example [sample data](/CensusData/SampleData.xlsx), please use the script [GenerateSampleData.Rmd](/GenerateSampleData.Rmd). <br> <br>
Required R packages are:
- [tidyverse](https://cran.r-project.org/web/packages/tidyverse/index.html)
- [openxlsx](https://cran.r-project.org/web/packages/openxlsx/index.html)
<br>
Make sure to change to working directory: `pathUse <- "/Users/douglasarneson/Documents/ButteLab/CovidPPIstudyVivek/FirstStudy/Analysis/DougResultsV1"`

## Running Analytical Pipeline
