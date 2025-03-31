---
layout: default
title: Weapon Laws – Data Story
---

<style>
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
</style>

# Weapon Laws – Data Story

*02806 | Social Data Analysis and Visualization | Spring 25 | Group 22*

---

## 🔎 Introduction

This website focuses on weapon-related crimes in San Francisco between 2008 and 2024.  
It shows how these crimes have changed over the years, influenced by major events and new policies.  
We also explore questions like: Have gun control policies really helped reduce weapon-related crimes?

In the FBI UCR (Uniform Crime Reporting) system and most US police datasets like SFPD Crime Data,  
**Weapon Laws** include:
- Possession of illegal weapons  
- Carrying weapons without permits  
- Violation of any statutory regulation of weapons  
- Felon in possession of a firearm  
- Illegal firearm sales or transfers  

It is *not* about using the weapon to commit a robbery, assault, or murder — those are separately classified.

---

## 📊 Overview: Weapon Laws Among All the Crimes

[📍 Your Bokeh chart will appear here later.]

---

## 🕒 Story in Time: What Happened in These Years?

Between 2008 and 2024, a total of **25,703 Weapon Laws** cases were recorded.  
The yearly proportions are shown in the **Total Counts**.

**Yearly Trend** shows a line chart illustrating the annual changes.  
**Monthly Counts** show monthly crime patterns per year.  
**Seasonal Pattern** highlights trends by month (e.g., Halloween spikes).  
**Hourly Trend** focuses on what time of day crimes peak.

👇 Click the buttons to explore each visualization:

<div style="margin-bottom: 1rem;">
  <button onclick="showChart('TimeSeries-1')">Total Counts</button>
  <button onclick="showChart('TimeSeries-2')">Yearly Trend</button>
  <button onclick="showChart('TimeSeries-3')">Monthly Counts</button>
  <button onclick="showChart('TimeSeries-4')">Seasonal Pattern</button>
  <button onclick="showChart('TimeSeries-5')">Hourly Trend</button>
</div>

<iframe id="TimeSeries-1" src="assets/TimeSeries-1.html" width="100%" height="600px" style="border:none;"></iframe>
<iframe id="TimeSeries-2" src="assets/TimeSeries-2.html" width="100%" height="600px" style="border:none; display:none;"></iframe>
<iframe id="TimeSeries-3" src="assets/TimeSeries-3.html" width="100%" height="600px" style="border:none; display:none;"></iframe>
<iframe id="TimeSeries-4" src="assets/TimeSeries-4.html" width="100%" height="600px" style="border:none; display:none;"></iframe>
<iframe id="TimeSeries-5" src="assets/TimeSeries-5.html" width="100%" height="600px" style="border:none; display:none;"></iframe>

<script>
function showChart(id) {
  const frames = ['TimeSeries-1', 'TimeSeries-2', 'TimeSeries-3', 'TimeSeries-4', 'TimeSeries-5'];
  frames.forEach(f => {
    document.getElementById(f).style.display = (f === id) ? 'block' : 'none';
  });
}
</script>

---

## 🧠 Time Trend Analysis & Key Policy Events

🔴 **2008–2011: Continuous Decrease**  
AB962 restricted ammunition sales → steady decline.  

🔴 **2011–2012: Increase**  
AB109 released prisoners → increased violations.

🔴 **2012–2013: Significant Increase**  
Sandy Hook shooting caused panic and rise in offenses.

🔴 **2014–2017: Continued Increase**  
Prop 47 lowered crime penalties → more violations.

🔴 **2017: Decline**  
Prop 63 restricted magazines → reduced cases.

🔴 **2018–2019: Further Decline**  
SB1100 raised gun purchase age → youth crimes dropped.

🔴 **2020–2021: Sharp Increase**  
COVID-19 → social unrest, nighttime spikes.

🔴 **2022–2024: Decline**  
AB1594 targeted gun industry → reduced sales-related crimes.

---

## 🗺️ Heatmap: Did Gun Laws Make SF Safer?

<iframe src="assets/map_crime.html" width="100%" height="600px" style="border:none;"></iframe>

📌 **2012–2015 (Before Prop 63):**  
Crimes concentrated in southeast areas (Bayview, Mission).

📌 **2017–2020 (After Prop 63):**  
Numbers rose, Tenderloin became new hotspot.

📌 **2023 (After SB 2):**  
Clear improvement. Crimes near schools dropped 89%.

---

## 🧾 Conclusion

> “**Laws can reduce crime overall, but not always change where it happens.**”  
> — *Prof. R. Gonzalez*

---

## 📚 Reference

- https://selfhelp.courts.ca.gov/  
- https://ballotpedia.org/California_Proposition_63  
- https://leginfo.legislature.ca.gov/

---

## 🤝 Contribution

**Bokeh:** Yu Zhang (s230000)  
**Time Series:** Shimin Huang (s242614)  
**Heatmap:** Yuling Zhai (s241613)
