# Stier Lab Coding Sessions

Weekly R and GitHub practice for undergraduates in the Ocean Recoveries Lab (Stier Lab) at UC Santa Barbara.

## Session 1: Getting to Know Our Reef Tank

Open `scripts/01_tank_intro.qmd` in RStudio and work through it from top to bottom. When you finish, click **Render** to turn it into a web page. You will:

1. Load real data from the Stier Lab aquarium
2. Explore it and calculate a few summary statistics
3. Make your first plots with ggplot2
4. Play detective and figure out what happened in the tank
5. Commit and push your work to GitHub

## Before you start

- Install [R](https://cran.r-project.org/) and [RStudio Desktop](https://posit.co/download/rstudio-desktop/)
- Create a [GitHub](https://github.com/) account
- Install the tidyverse by running `install.packages("tidyverse")` in the RStudio console

## The data

`data/tank_data.csv` holds 2,123 readings recorded every 10 minutes from October 9 to October 23, 2026 by the tank's Neptune Apex controller. Each row is one moment in time.

| Column | What it measures | Units |
|---|---|---|
| `datetime` | Date and time of the reading (Pacific time) | Year-month-day hour:minute:second |
| `date` | Date only | Year-month-day |
| `hour` | Hour of the day | 0 (midnight) to 23 (11 p.m.) |
| `temperature` | Water temperature | Degrees Fahrenheit |
| `ph` | pH (acidity) | pH units |
| `orp` | Oxidation reduction potential, a measure of water quality | Millivolts |
| `salinity` | Salinity, measured by conductivity | Parts per thousand |
| `alkalinity` | Carbonate alkalinity, tested every 6 hours | Degrees of carbonate hardness |
| `calcium` | Calcium, tested every 6 hours | Parts per million |
| `magnesium` | Magnesium, tested every 6 hours | Parts per million |
| `light_watts` | Power used by the light | Watts |
| `heater_watts` | Power used by the heater | Watts |
| `return_pump_watts` | Power used by the return pump (moves water from the sump to the display) | Watts |
| `skimmer_watts` | Power used by the protein skimmer | Watts |
| `uv_sterilizer_watts` | Power used by the ultraviolet sterilizer | Watts |

## About the tank

The Stier Lab aquarium is a reef display tank with a sump underneath, which holds the temperature, salinity, pH, and oxidation reduction potential probes, plus a refugium with macroalgae and live rock. It is used mainly to grow stony corals like *Stylophora*, *Acropora*, and *Montipora*, which lab members use for experiments.
