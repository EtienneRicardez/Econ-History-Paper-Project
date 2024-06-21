# Local Institutions in Economic Development: The Effect of Juntas Auxiliares in Puebla, Mexico

## Description

This project measures the effect of a local institution called 'Juntas de Auxiliares' in the state of Puebla, Mexico, on household income at the municipality level. The analysis involved collecting information on the number of Juntas de Auxiliares for 172 municipalities out of the 215 in Puebla. To address potential endogeneity issues, territorial extension of the municipalities was used as an instrument to calculate the number of Juntas de Auxiliares.

## Data Sources

1. **Income per Household**: Data from the National Institute of Statistics and Geography (INEGI). Available at: [INEGI ICMM 2020](https://en.www.inegi.org.mx/investigacion/icmm/2020/)
2. **Territorial Extension**: Data on the territorial extension of each municipality in Mexico. Available at: [INEGI Census 2020](https://www.inegi.org.mx/programas/ccpv/2020/tableros/panorama/)
3. **Geographical Coordinates**: Latitude, Longitude, and Altitude of each municipality in Mexico. Available at: [INEGI AGEEML](https://www.inegi.org.mx/app/ageeml/)
4. **Indigenous Population Percentage**: Estimates of the indigenous population percentage by municipality in Mexico. Available at: [INPI Indicators 2020](https://www.inpi.gob.mx/indicadores2020/)
5. **Number of Juntas Auxiliares**: Compiled manually through detailed investigation of official municipal websites, contact with municipal headquarters, and review of various academic and journalistic publications. This data covers 172 out of 215 municipalities in Puebla, totaling 658 Juntas Auxiliares.

## Methodology

The methodology involves several steps:

1. **Data Compilation**: Combine data on household income, territorial extension, geographical coordinates, indigenous population percentage, and the number of Juntas Auxiliares into a single dataset.
2. **Cleaning and Preparation**: Ensure the names of municipalities match the GeoFIPS codes for accurate merging.
3. **Simple OLS Models**: Measure the impact of the number of Juntas Auxiliares on household income using different OLS model specifications.
4. **Instrumental Variables (IV)**: Address endogeneity by using the territorial extension of each municipality as an instrument for the number of Juntas Auxiliares.
5. **Falsification Tests**: Conduct 31 falsification tests using municipalities from other states to defend the validity of the instrument.

## Key Findings

The study found that Juntas Auxiliares are significantly associated with a 2% increase in household income, indicating their positive contribution to local economic development. The use of territorial extension as an instrument was validated through 31 falsification tests, reinforcing the robustness of the findings.

## Requirements

- R
- dplyr
- tidyverse
- stringr
- readr
- stargazer
- broom
- AER
- pander

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/EtienneRicardez/Econ-History-Project.git
2. Navigate to the project directory:
   ```sh
   cd Econ-History-Project
3.- Install required packages in R:
   ```sh
   install.packages(c("dplyr", "tidyverse", "stringr", "readr", "stargazer", "broom", "AER", "pander"))
   ```

## Usage
## Installation

Run the main script to start the data processing and interpolation:
  ```sh
  source("main.R")
  ```

## Acknowledgments

I want to thank and give credit to many people, without whom this research would not have been possible. First to my brother, Ray Ricardez, who had let me be an indirect part of his work as a journalist and thanks to that, I was able to learn about Juntas Auxiliares. Secondly, to Felipe Valencia Caicedo, who always listened to me and guided me to develop this research. To Nathan Nunn's classes that, in the company of Ines Moran and Carla Colina, were the trigger for this idea. To Elliot Grenier who, making breakfast, almost destroyed this article, but thanks to him, I had the idea of the falsification tests. To Chanya Chawla, who made me believe again that my prime hasn’t passed yet. To Vicente Guerra and Guillermo Parra for their feedback, laughs and support. And, obviously, to my parents.
