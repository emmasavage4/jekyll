---
name: hw 8 Project
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

<vegachart schema-url="{{ site.baseurl }}/assets/visualization.json" style="width: 100%"></vegachart>


# writeup
My first visualization is a scatter plot that visualizes the relationship between floors above grade and the total floors in the data set. Each point represents a point in the data set. My x axis is “Floors Above Grade” and my y -axis represents “total floors.” The color is based on the conditional selected_floors. When the points are selected they are colored green and the non selected points are colored grey. I chose green and grey to help the user distinguish between selected and not selected data points. I used alt.condition()  to color the points based on selected_floors. For interactivity I used the selected_floors selection. This allows the users to select points which change color.
My second visualization shows the distribution of the sum of total floors across different bins of floors above grade. I chose a bar plot to show the sum of total floors in each bin. My x-axis is “Floors Above Grade” binned and the Y-axis is the sum of “Total Floors.” I chose the color scheme to be green. I chose this to remain consistent with my other chart. I used transform_filter(selected_floors) to filter the data based on the selection. I also used .aggregate(‘sum’) to aggregate the sum of “Total Floors.”
In hw 7 and hw 8 I used the same data set and also decided to use the same columns from the data set to create visualizations. The difference between my homework 7 and 8 is that I am using Altair for my visualizations in 8. I also added interactivity in my visualization for 8, so the user can select points on the graph and it will change colors based on which points are selected. I also changed the color scheme to green for both the visualizations. For the first visualization green is the color of the point when it is selected and it is grey when it is not selected. 
# Example including vega-lite

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/emmasavage4/jekyll/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

