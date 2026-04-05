# Sofia-AQ

# What Is Actually Making Sofia's Air Dirty?
## A Multi-Predictor Regression Study of Particulate Matter in Sofia, Bulgaria

---

> *"You can't improve what you can't measure — and you can't measure what you haven't separated."*

---

Sofia consistently ranks among the most polluted EU capitals. Every winter, a thick grey smog settles over the city — a visible sign of dangerously high concentrations of **particulate matter (PM)**, microscopic solid and liquid particles suspended in the air small enough to be inhaled deep into the lungs. The most regulated size fraction is **PM10** — particles under 10 micrometres in diameter — for which the EU sets a legal annual average limit of 40 µg/m³. Sofia routinely exceeds it.

The usual suspects are well known: wood-burning stoves, old diesel cars, industrial activity. But Bulgaria's electricity grid has also changed dramatically — lignite (brown coal) generation collapsed 59% in 2024, with CO₂-free sources now comprising 66% of the power mix.

So here is the question nobody has cleanly answered: **does grid-level decarbonization actually show up in Sofia's air quality (AQ), or is the signal completely buried under heating season and weather?**

To answer it, we can't just plot energy mix against pollution and call it correlation. We have to control for the things that dominate — temperature, wind, the heating season — and then look at what's left. That remainder, if anything, belongs to the grid.

We will:
1. Collect and merge three independent data sources: EEA station-level PM10 measurements, ENTSO-E hourly generation data for Bulgaria, and ERA5 meteorological reanalysis via Open-Meteo
2. Explore the data and establish the seasonal and meteorological structure of Sofia's PM10 exceedances
3. Build a multiple linear regression model with heating season, wind speed, temperature, and lignite generation share as predictors
4. Quantify the partial effect of the energy mix after controlling for the dominant confounders
5. Cross-validate findings using a Random Forest model and compare feature importances
6. Interpret the result honestly — including if the grid signal doesn't survive the controls

---

Author: Teodor Evgeniev (@TeodorEvgeniev)
