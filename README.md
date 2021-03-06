# WiP-Tidy-Data-dt
Exercise for R-datatable-Tidy-Data Repo

<img src="images/Women_in_Parliament_hex.svg" alt="Women in Parliament Hex Sticker" width="400"> 

## World Bank "Women in Parliament" Data

The raw data for *"Proportion of seats held by women in national parliaments"* 
(_"single or lower parliamentary chambers only"_) by can be directly downloaded from:

+ https://data.worldbank.org/indicator/SG.GEN.PARL.ZS 

As part of its "open data" mission the World Bank kindly offers *"free and open access to 
global development data"* licensed under the "Creative Commons Attribution 4.0 (CC-BY 4.0)".

### Source Data

The data originates from the ["Inter-Parliamentary Union" (IPU)](https://www.ipu.org/)
which provides an *"Archive of statistical data on the percentage of women in 
national parliaments"* going back to 1997 on a monthly basis:

+ http://archive.ipu.org/wmn-e/classif-arc.htm

The World Bank data is for “single or lower parliamentary chambers only”, while 
the IPU also presents data for “Upper Houses or Senates”. Moreover, the IPU provides 
the actual numbers used to calculate the percentages (which the World Bank does not).
The data has to be scraped from the IPU website (please check the `robots.txt` file
first).

### Importing the Raw Data into R

First download the latest `CSV` file from:

+ https://data.worldbank.org/indicator/SG.GEN.PARL.ZS 

Below I will refer to this file as "`WiP-Data.csv`" but please use the actual
file name that you save it as.

#### Using `data.table`

```
library(data.table)
wipdt <- fread("WiP-Data.csv",
               skip = 4, header = TRUE, check.names=TRUE)
```

<img src="images/Women_in_Parliament_rect.svg" alt="Women in Parliament Bonus Image" height="400"> 

## Acknowledgements

The images were create by [Marina Costa](https://cargocollective.com/marinacostaportfolio/ABOUT) 
guided by [Andreia Carlos](https://github.com/agrou) and myself. 

You can view Marina's great portfolio at:

+ https://cargocollective.com/marinacostaportfolio

