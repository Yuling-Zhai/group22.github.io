---
layout: default
title: Weapon Laws – Data Story
---

<style>
.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  line-height: 1.6;
}
.site-header,
.site-title,
.site-nav,
footer,
h2.post-list-heading,
ul.post-list,
.post-meta {
  display: none !important;
}
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

📍 *Your Bokeh chart will appear here later.*

---

## 📅 Story in Time: What Happened in These Years?

Between 2008 and 2024, a total of **25,703 Weapon Laws cases** were recorded.

### 🔘 Explore the Charts

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
AB962 restricted ammunition sales — cases gradually declined.

### 🔴 2011–2012: Sudden Increase  
AB109 released prisoners — sharp rise in violations.

### 🔴 2012–2013: Spike  
Sandy Hook shooting caused national fear — more reports.

### 🔴 2014–2017: Continued Rise  
Prop 47 reduced crime penalties — increased weapons violations.

### 🔴 2017: Decline  
Prop 63 implemented magazine limits — slight drop in cases.

### 🔴 2020–2021: Peak  
COVID-19 unrest, policy shifts — major spikes.

### 🔴 2022–2024: Decrease  
AB1594 gun industry liability — fewer sales-related cases.

---

## 🔥 Heatmap: Tracing Weapon Crime Before and After California’s Gun Laws

California’s weapon laws got progressively tougher — Prop 63 in 2016 added ammo restrictions, and SB 2 in 2023 banned guns near schools, parks, and other “sensitive places.”  
But how did these policies actually shape public safety in San Francisco?

<iframe src="assets/map_crime.html"></iframe>

### 🧭 What Changed Across Time?

#### 📍 2012–2015 (Before Prop 63)  
**5,861 cases** — mostly concentrated in the southeast: **Bayview**, **Mission**  
Western neighborhoods like **Richmond** and **Sunset** stayed relatively safe.

#### 📍 2017–2020 (After Prop 63)  
Cases rose to **6,090** despite new laws.  
Some southern districts saw minor drops, but **Bayview** and **Tenderloin** remained hotspots.

#### 📍 2021–2022 (Pre-SB 2)  
Cases dropped to **3,608**, possibly due to **pandemic effects**.  
Hot zones stayed hot, while western areas grew even quieter.

#### 📍 2023–2024 (After SB 2)  
Slight increase to **3,402 cases**.  
Parks and schools saw **some reduction**, but hotspots remained — suggesting **partial**, not full, policy success.

---

### 🔎 What the Map Tells Us

✅ **Gun-free zones help, but aren’t a silver bullet**  
❗ **Crime shifted but didn’t vanish** — Mission and Bayview still dominate  
⚖️ **Effective policy** = legal reform + community investment

> “Regulation alone can’t erase the geography of crime.”  
> — *Prof. R. Gonzalez, UC Berkeley*

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
