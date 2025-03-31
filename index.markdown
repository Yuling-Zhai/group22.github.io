---
layout: default
title: Weapon Laws – Data Story
---

<style>
/* Centered content container */
.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  line-height: 1.6;
}

/* Hide Jekyll default theme elements */
.site-header,
.site-title,
.site-nav,
footer,
h2.post-list-heading,
ul.post-list,
.post-meta {
  display: none !important;
}

/* Button styles */
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

/* Frame styling */
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

This website explores weapon-related crimes in San Francisco (2008–2024), analyzing how crime patterns evolved over time and how new gun control laws like Proposition 63 and SB 2 may have influenced public safety.

In FBI UCR and most police datasets, **Weapon Laws** include:
- Possession of illegal weapons  
- Carrying weapons without permits  
- Violation of weapon regulations  
- Felon in possession of a firearm  
- Illegal firearm sales or transfers  

This does *not* include assault or robbery using a weapon — those are classified differently.

---

## 📊 Overview: Weapon Laws Among All the Crimes

[📍 Your Bokeh chart will be embedded here.]

---

## 📅 Story in Time: What Happened in These Years?

Between 2008 and 2024, a total of **25,703 Weapon Laws cases** were recorded.

### 🔘 View the charts

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

### 🔴 2008–2011: Continuous Decrease  
AB962 limited ammo sales — weapon-related cases dropped gradually.

### 🔴 2011–2012: Sudden Increase  
AB109 released prisoners and indirectly increased weapon-related cases.

### 🔴 2012–2013: Major Rise  
Sandy Hook mass shooting may have triggered panic-related enforcement and reporting.

### 🔴 2014–2017: Continued Increase  
Prop 47 lowered penalties — possibly encouraging more violations.

### 🔴 2017: Decline  
Prop 63 restricted ammo and magazine sales — some drop observed.

### 🔴 2020–2021: Sharp Rise  
COVID-19, protests, and police focus shift likely influenced crime spikes.

### 🔴 2022–2024: Noticeable Decline  
AB1594 held gun manufacturers accountable — may have helped reduce crimes.

---

## 🗺️ Heatmap: Did Gun Laws Make San Francisco Safer?

<iframe src="assets/map_crime.html"></iframe>

### 📍 District-level Insights

- **2012–2015 (Before Prop 63):** Crime concentrated in Bayview & Mission  
- **2017–2020 (After Prop 63):** Total cases rose; Tenderloin emerged as a new hotspot  
- **2023 (After SB 2):** Big drop (−71%); parks and schools became much safer

---

## 📚 References

- https://selfhelp.courts.ca.gov/  
- https://ballotpedia.org/California_Proposition_63  
- https://leginfo.legislature.ca.gov/

---

## 🙌 Contribution

**Bokeh:** Yu Zhang (s230000)  
**Time Series:** Shimin Huang (s242614)  
**Heatmap:** Yuling Zhai (s241613)

</div>
