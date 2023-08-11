# Plots for Eurostat data with R
Experience the magic of data visualization with my Eurostat project! Join me on an exciting journey as I take my first steps in using R to recreate Eurostat's visuals. 

![Collage Maker-17-Jul-2023-04-14-PM-3913](https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/7477a612-47d0-4273-80b3-1fb8d0687e9b)

## Introduction

As a statistical consultant in a consultancy firm, I had the opportunity to work on an exciting project with Eurostat from 2020-2021. The project involved providing statistical articles for their ["What's New"](https://ec.europa.eu/eurostat/web/main/news/news-articles) section, and I played a vital role in analyzing data, writing articles, and collaborating with the graphic designer to produce visuals using Adobe Illustrator. We submitted over 100 articles and double the number of visuals, which were published on Eurostat's website.

During the project, I seized the chance to enhance my R skills by recreating some of the visuals using R for my personal archive. I explored various types of visuals, which helped me gain a better understanding of how to use R effectively to create a wide range of data visualizations. All data used for this project are openly accessible to the public.

This post will showcase ten of these graphs, accompanied by the R code. You will discover the challenges I encountered, such as formatting data to meet R's requirements, selecting appropriate colors and fonts for charts, and adjusting plot sizes and labels for readability. However, these challenges also provided me with ample opportunities to learn new techniques and problem-solving strategies.

I hope you enjoy this portfolio and find these visualizations informative and engaging.

Thank you for taking the time to explore my work.

Let's get started!

Before we start, check [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L1-L10) the libraries that I used.

## 1. Line chart with R base plot

The first visualization is a line chart that shows the production of chemicals in the European Union. The data comes from Eurostat and shows that the production of industrial chemicals increased in 2018 compared to the previous three years, but it's still lower than the peak in 2007. A line chart is a good choice for this data because it shows how the production of chemicals has changed over time.

To create the line chart, I downloaded the data from Eurostat and saved it as an Excel file on my local drive. Then, I used R Base graph plot to create the chart and set the background, margins, and axis labels. I added three lines to the plot: one for total chemicals, one for hazardous chemicals to health, and one for hazardous chemicals to environment. I adjusted the x-axis values, added a title and subtitle to the plot, and created a legend for the three lines. I also added a text label to the top of the plot and drew grid lines to make it easier to read. The final result could be said to bear a slight resemblance to the original one.


|Article	| Details|
|---------|---------|
|Topic	|Production of chemicals in the EU|
|Publication date	|21/1/2020|
|Link	|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/ddn-20200121-1|
|Data	| Eurostat’s database: Production and consumption of chemicals by hazard class|
|Variables | Hazardous and non-Hazardous-Total,Hazardous to health, Hazardous to environment,Year, Time|
|Reference |For more information about the production of chemicals in the EU, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Chemicals_production_and_consumption_statistics).

### Code & plot
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L14-L52)

## 2. Dumbbell chart with gglpot2
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L55-L128)
## 3. Barchart with R base
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L132-L154)
## 4. Line chart with R Base plot
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L158-L187)
## 5. Small multiples pie charts with ggplot2
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L190-L233)
## 6. Stacked bar chart with ggplot
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L235-L278)
## 7. 100% stacked barchart with ggplot2
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L282-L311)
## 8. Scatterplot
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L314-L330)
## 9. Treemap
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L334-L351)
## 10. Horizontal barplot
Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L354-L375)


