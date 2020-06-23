---
title: "Visualizing the Spread & Effects of COVID-19 Around the World"
date: 2020-05-11
excerpt: "Building a reporting dashboard to display the effects of COVID-19 globally.<br/><img src='/images/COVIDdash.png' style='width:395px;height:254px;'>"
collection: portfolio
---

## Summary

Amidst the COVID-19 pandemic, we found common interest in applying advanced python methods to build a visualization dashboard that investigates its effects. We choose three particular areas of interest:
1. Economic effects (measured by relative change in stock price based on each company’s range from November 2019 to January 2020)
2. Social effects (measured by volume of Twitter activity per day per geography)
3. Public health effects (measured by total fatalities per day per geography).

Report can be found [here](https://github.com/zivschwartz/Coronavirus_Analysis/blob/master/group01_report.pdf), slides [here](https://github.com/zivschwartz/Coronavirus_Analysis/blob/master/group01_presentation.pdf) and relevant code can be found [in this GitHub repo](https://github.com/zivschwartz/Coronavirus_Analysis).

**Data and Methods** 

Wanting to present the data in a cohesive manner, we use Python’s plotly visualization package with dash, which together enable us to produce a single sub-plotted visualization with a universal slider to provide a dynamic time series view of daily change. Given the scale and limitations of some of our data and collection capacities (e.g., Twitter's API call restrictions forced us to seek other data sourcing), we gather data from January 21st onward, a reasonable negotiation given the timeline of the global spread of COVID-19 which escalated mostly after mid-January.

The dashboard layout is as follows:
1. New COVID-19 cases reported per day
2. Daily COVID-19 tweets
3. Normalized stock index
4. Hypothesized stock index

<p align="center">
  <video src="/images/group01_results_sm.mov" width="550" height="350" controls preload></video>
</p>

To launch the application:
- Git clone [repository](https://github.com/zivschwartz/Coronavirus_Analysis)
- Initialize Virtual Environment
- $ pip install -r requirements.txt
- $ python3 app.py
