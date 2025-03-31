---
layout: default
title: SF Crime Micro Project
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

# 🔫 Weapon Crime in San Francisco: A Short Data Story

## 🧭 Introduction

This project explores how weapon-related crimes in San Francisco evolved over the past decade, particularly before and after two major California gun control policies: Proposition 63 (2016) and Senate Bill 2 (2023).

---

## 📈 1. Weapon Crime Time Series (2012–2024)

Explore trends by clicking the buttons below to switch between visualizations:

<div style="margin-bottom: 1rem;">
  <button onclick="showChart('TimeSeries-1')">Trend 1</button>
  <button onclick="showChart('TimeSeries-2')">Trend 2</button>
  <button onclick="showChart('TimeSeries-3')">Trend 3</button>
  <button onclick="showChart('TimeSeries-4')">Trend 4</button>
  <button onclick="showChart('TimeSeries-5')">Trend 5</button>
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

*Figure 1: A series of time-based visualizations showing weapon-related crimes from 2012 to 2024.*

---

## 🗺️ 2. Weapon Crime by District (Heatmap)

<iframe src="assets/map_crime.html" width="100%" height="600px" style="border:none;"></iframe>

*Figure 2: District-level heatmap of weapon-related crimes before and after major policy changes.*

---

## 📚 Conclusion

We observe some visible shifts in weapon-related crime patterns over time and across locations. Further analysis is needed to confirm causal links to policy changes.

---

## 🔗 References

- [San Francisco Police Department Data Portal](https://data.sfgov.org)
- [California Proposition 63 Overview](https://ballotpedia.org/California_Proposition_63,_Firearms_and_Ammunition_Sales_(2016))
- [California Senate Bill 2 (2023)](https://leginfo.legislature.ca.gov/)
