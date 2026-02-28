---
title: "Analyzing Sakura bloom trends in Japan"
excerpt_separator: "<!--more-->"

--- 


Our projects attempt to **Visualize Cherry Blossom Bloom Trends Across Japan** by training a machine learning model on sakura flower bloom reccords and real geospacial NASA termperature and precipitation data. This project was done for the 2026 NASA Space Apps Hackathon. More information about the hackathon submission can be found on our github (button below). 


<!-- <img src="/assets/images/hanami_Ben.PNG" width="400"> -->


<div style="display:flex; gap:10px; align-items:flex-start;">
  <!-- Right column: two stacked landscape images -->
  <div style="display:flex; flex-direction:column; gap:10px; width:50%;">
    <img src="/assets/images/hanami_full.png" style="width:100%; border-radius:8px;"> 
    <img src="/assets/images/hanami_Screenshot.png" style="width:100%; border-radius:8px;">
  </div>

  <!-- Left column: portrait image -->
  <div style="width:50%;"> 
    <img src="/assets/images/hanami_Ben.PNG" style="width:100%; border-radius:6px;"> 
  </div>
</div>

<!-- Button -->
<p>
  <a href="https://github.com/Kanahe1800/hanami-bloom-prediction" class="btn btn--primary">
    View GitHub for code
  </a>
</p>

---

## Motivation  
Japan attracts an average of 30–40 million tourists each year [1], many drawn by the country’s breathtaking natural scenery and particularly beautiful annual **cherry blossom bloom**.  

Beyond tourism, bloom timing also acts as a **biological sensor** for environmental change. Shifts in the time of full blooming can reflect variations in temperature, precipitation, and CO₂ emissions, serving as indicators of climate change.  

Our goal is twofold:
1. Help travelers find the best times to visit Japan for cherry blossoms 
2. Investigate how environmental factors influence bloom timing and plant health  

---
## Solution

Our approach models bloom timing as a regression problem, where the target variable is the week of the year (1–52) in which sakura reach full bloom. We trained and compared multiple models, including:
- Linear Regression
- Polynomial Regression
- random forest
- Neural Networks
- Random Forest Regression (best performing model) [2]

To make the model accessible, we developed a simple web interface where users can:
- Select a city in Japan
- Input or retireve relevant climate features
- View the predicted bloom week

This allows travelers and researchers to explore how climate conditions influence bloom timing in an intuitive way. 

<img width="882" height="633" alt="Screenshot 2025-10-04 at 10 48 07 PM" src="/assets/images/hanami_Screenshot.png" />
  

---

## Methodology  
We used **OpenEarthData API** [3] to collect environmental data for Japan, spanning 1981 to the present day, including:

- **Monthly mean temperature (in Degrees Celcius):** `M2SMNXSLV`  
- **Number of days with rainfall >= 1mm per month:** `M2SMNXEDI`  

For each year X, we gathered data from November (X) to March (X + 1) to capture both:

- **Spring forcing temperature** – drives the onset of blooming  
   **Winter chill requirement** – ensures plants are ready for spring growth  

We used data from the Japan Meteorological Agency (JMA) for the historic Full bloom week records and site data.

We then constructed seasonal tables and visualizations to identify long-term climate patterns and their correlation with cherry blossom timing, guided by plant phenology research [4].

---

## Future Applications  
- Monitoring other climate phenomenom with predictions, such as CO2 emission, N2 desposition, and photoperiod
- Scaling the model to other regions and plant species  accross the globe
- Providing tourism recommendations based on real-time environmental data  

---

## References  
1. [Japan National Tourism Organization – Inbound Statistics](https://www.tourism.jp/en/tourism-database/stats/inbound/)
2. [Sakura Flower Bloom-Prediction Full Project Final Report](https://github.com/Tristant2005/474-Sakura-Project/blob/main/474%20Final%20Report.pdf)
3. [OpenEarthData API – MERRA-2 Dataset](https://disc.gsfc.nasa.gov/datasets/M2SMNXSLV_5.12.4/summary)  
4. [Frontiers in Plant Science – Understanding Blooming Responses to Climate Change](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2020.00443/full)