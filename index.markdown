---
layout: default
title: Weapon Laws – Data Story
---

<style>
/* 居中容器 */
.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  line-height: 1.6;
}

/* 隐藏 GitHub Pages 的默认导航栏等 */
.site-header,
.site-title,
.site-nav,
footer,
h2.post-list-heading,
ul.post-list,
.post-meta {
  display: none !important;
}

/* 按钮样式 */
button {
  padding: 8px 14px;
  margin-right: 6px;
  margin-bottom: 10px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 500;
}
button:hover {
  background-color: #e2e2e2;
}

/* 图表统一尺寸 */
iframe {
  width: 100%;
  height: 600px;
  border: none;
  margin-bottom: 1.5rem;
}
</style>

<div class="container">

# Weapon Laws – Data Story

**02806 | Social Data Analysis and Visualization | Spring 25 | Group 22**

---

## 🔎 Introduction

This website explores weapon-related crimes in San Francisco (2008–2024), examining how crime levels shifted over time and in relation to new legislation like Proposition 63 and Senate Bill 2.

**Weapon Laws** in crime data include:
- Possession of illegal weapons  
- Carrying weapons without permits  
- Felon in possession of a firearm  
- Illegal firearm sales or transfers

We ask: *Did gun control laws really reduce weapon-related crimes?*

---

## 📊 Overview: Weapon Laws Among All the Crimes

[📍 Your Bokeh chart will appear here later.]

---

## 📅 Story in Time: What Happened in These Years?

Between 2008–2024, a total of **25,703 Weapon Laws** cases were recorded. Explore the visualizations below:

<div style="margin-bottom: 1rem;">
  <button onclick="showChart('TimeSeries-1')">Total Counts</button>
  <button onclick="showChart('TimeSeries-2')">Yearly Trend</button>
  <button onclick="showChart('TimeSeries-3')">Monthly Counts</button>
  <button onclick="showChart('TimeSeries-4')">Seasonal Pattern</button>
  <button onclick="showChart('TimeSeries-5')">Hourly Trend</button>
</div>

<iframe id="TimeSeries-1" src="assets/TimeSeries-1.html"></iframe>
<iframe id="TimeSeries-2" src="assets/TimeSeries-2.html" style="display:none;"></iframe>
<iframe id="TimeSeries-3" src="assets/TimeSeries-3.html" style="display:none;"></iframe>
<iframe id="TimeSeries-4" src="assets/TimeSeries-4.html" style="display:none;"></iframe>
<iframe id="TimeSeries-5" src="assets/TimeSeries-5.html" style="display:none;"></iframe>

<script>
function showChart(id) {
  const frames = ['TimeSeries-1', 'TimeSeries-2', 'TimeSeries-3', 'TimeSeries-4', 'TimeSeries-5'];
  frames.forEach(f => {
    document.getElementById(f).style.display = (f === id) ? 'block' : 'none';
  });
}
</script>

---

## 🧠 Timeline: Law Impacts & Interpretations

🔴 **2008–2011: Decrease** – AB962 restricted ammunition sales.  
🔴 **2011–2012: Spike** – AB109 released prisoners.  
🔴 **2012–2013: Rise** – Sandy Hook shooting.  
🔴 **2014–2017: Rise** – Prop 47 reduced sentencing.  
🔴 **2017: Drop** – Prop 63 restrictions began.  
🔴 **2020–2021: Spike** – COVID and social unrest.  
🔴 **2022–2024: Decline** – AB1594 gun industry liability.

---

## 🗺️ Heatmap: Did Gun Laws Make SF Safer?

<iframe src="assets/map_crime.html"></iframe>

🧭 **District Summary:**

- **2012–2015 (Before Prop 63):** Crime clustered in Bayview, Mission  
- **2017–2020 (After Prop 63):** Total increased; Tenderloin hotspot  
- **2023 (After SB 2):** Drop by 71%; safer around parks/schools

---

## 📚 References

- https://selfhelp.courts.ca.gov/  
- https://ballotpedia.org/California_Proposition_63  
- https://leginfo.legislature.ca.gov/

---

## 🙌 Contribution

**Bokeh:** Yu Zhang (s230000)  
**Time Series:** Shimin Huang (s242614)  
**Heatmap:** Yulin Zhai (s241613)

</div>
