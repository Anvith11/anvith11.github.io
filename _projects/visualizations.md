---
name: Homework 5
tools: [Python, HTML, altair, vega-lite]
image: assets/pngs/hw5.jpg
title: Visualization Assignment - Homework 5
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# 🧠 Visualization Assignment — Homework 5

Below are two visualizations created using **Python + Altair + Vega-Lite** based on the University of Illinois building inventory dataset.

Each chart was exported to `.json` from the Python notebook and embedded here using **Vega-Embed** for interactivity.

---

## 🏙️ Plot 1: Distribution of Buildings by City and Building Type

This visualization shows how building types are distributed across different **cities** in the University of Illinois building inventory dataset. The x-axis encodes each city, while the y-axis represents the **number of buildings** recorded in that city. Building types are represented using color to help distinguish categories and reveal local architectural trends.  

Using a **bar chart encoding**, I mapped `City` to the x-axis (nominal) and `count()` to the y-axis (quantitative). Colors encode the `Building Type` (nominal), allowing quick visual comparison between types across cities. The “category10” color scheme was used to maintain accessibility and clarity.  

No major data transformations were needed beyond filtering out null city values in Python. The result offers an easy way to identify which cities have the largest building inventories and what types dominate those regions.

<!-- <h2>Plot 1: City vs Building Count</h2>
<p>Write-up paragraph about what you visualized, encodings, color, etc.</p>
<div id="vis1"></div>
<script type="text/javascript">
vegaEmbed('#vis1', 'https://python_notebooks/plot1.json');
</script> -->

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>

<!-- <vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart> -->
---

## 🏗️ Plot 2: Relationship Between Year Acquired and Square Footage

This plot visualizes the relationship between **the year a building was acquired** and its **square footage**, grouped by city. Each point represents a building. The x-axis shows `Year Acquired`, and the y-axis encodes `Square Footage`. The color encodes `City`, helping us see how acquisition timelines differ across locations.

The chart includes **interactive selection**: when hovering or selecting a city, related points are highlighted while others fade, making temporal and spatial trends clearer. This interactivity adds depth by allowing viewers to isolate cities and explore acquisition trends dynamically.  

In data preparation, I filtered out buildings with missing or invalid year or square footage values and ensured that the x-axis starts slightly below the minimum year (for cleaner presentation).

<!-- <h2>Plot 2: Year Acquired vs Square Footage</h2>
<p>Write-up paragraph about what you visualized and interactivity.</p>
<div id="vis2"></div>
<script type="text/javascript">
vegaEmbed('#vis2', 'python_notebooks/plot2.json');
</script> -->

<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

---

## 🧩 Technical Details

These visualizations were created in a Jupyter notebook using Python, Pandas, and Altair, then exported as JSON specifications (`plot1.json` and `plot2.json`) and embedded here using Vega-Lite.

## Data & Methods
Link to Data:
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Anvith11/Anvith11.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
