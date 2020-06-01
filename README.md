### [US China Trade War Tracker](https://www.tradewartracker.com/)

---
![](docs/web_banner.png)

**About the Tracker:** ​The goal is simple: Visually track the US and China trade war, provide easy access to the data and code behind the presentation, do so in a way that is essentially "live" (as the US census releases the data, the data and figures will be automatically updated).

**About the Repository:** Again the goal is to provide easy access to the data and resources to better understand the Phase One Trade Agreement and the Trade war. The code repository contains all the notebooks; almost all code is directly fetched from US government sources.

Clean up of the repo is in progress, basic outline is described below.

---
#### [Phase-One Tracker](https://www.tradewartracker.com/)

There are several components to creating these visuals.

  - [make-phase-one-product-list.ipynb](make-phase-one-product-list.ipynb) creates the list of products that are coverd by the [Phase One aggreement in Annex 6-1](notes/Economic_And_Trade_Agreement_Between_The_United_States_And_China_Text.pdf).

  - [phase-one-trade.ipynb](phase-one-trade.ipynb) grabs the trade data, product list, and then county-level informaiton to creat the figures on the main site.

  - [phase-one-plots.ipynb](phase-one-plots.ipynb) creates the plots for the first panel on the website (goals and time series plots).

  - [phase-one-map.ipynb](phase-one-map.ipynb) creates the map of the county level gain in exports per worker to China. To get the shapefiles for the maps, run [download_shapefiles.ipynb](download_shapefiles.ipynb)

---

#### [Trade War: Time, Products, Region](https://www.tradewartracker.com/the-us-china-trade-war.html)

  - [make-us-tariffs.ipynb](make-us-tariffs.ipynb) constructs the US, Section 301 tariff actions from orginal source data (see the notebook for details and [here for some notes](notes/section301-tariffs.md)).

  - [us-china-imports.ipynb](us-china-imports.ipynb) grabs US imports and makes the US import tariff series. Note the export series is just taken from [Consumption Response to Trade Shocks repo](https://github.com/mwaugh0328/consumption_and_tradewar), need to fix this part so it's stand alone.

  - [county-projection-imports.ipynb](county-projection-imports.ipynb) projects the US import tariff series down to the county-level by constructing an employment weighted average across industries.

  - [county-projection-exports.ipynb](county-projection-exports.ipynb) projects the China tariff on US exports down to the county-level by constructing an employment weighted average across industries.

  - [trade_plots_us.ipynb](trade_plots_us.ipynb) creates the graphic with the map, time series plot of US tariffs on imports from China, break down by NAICs industry catagory.

  - [trade_plots_china.ipynb](trade_plots_china.ipynb) creates the graphic with the map, time series plot of Chinese tariffs on US exports, break down by NAICs industry catagory.
