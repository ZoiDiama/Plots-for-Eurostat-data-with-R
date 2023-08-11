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
|Data	| Eurostat’s database: [Production and consumption of chemicals by hazard class](https://ec.europa.eu/eurostat/databrowser/view/ENV_CHMHAZ__custom_6892428/default/table?lang=en)|
|Variables | Hazardous and non-Hazardous-Total,Hazardous to health, Hazardous to environment,Year, Time|
|Reference |For more information about the production of chemicals in the EU, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Chemicals_production_and_consumption_statistics).

### Code & plot
<img width="479" alt="1" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/15b7d3c0-b3c6-4083-be1f-268874832d46">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L14-L52).

## 2. Dumbbell chart with gglpot2
The second plot I’m sharing shows the employment rate of women and men in the European Union (EU) in 2018, highlighting the difference between the two rates. To create this visualization, I experimented with two different chart types - a dumbbell chart and a bar chart. In this section, I’ll describe the dumbbell chart.

A dumbbell chart is a good choice for comparing the difference between two values across multiple categories. To create the dumbbell chart, I used the ggplot2 package in R. First, I imported the data from an Excel file and renamed the first column. Then, I calculated the difference between the employment rate of men and women and put the data into long format.

Next, I used the ggplot function to create the dumbbell chart. Each country is represented by a pair of dots - one for men and one for women - and these dots are connected by a line, making it easy to see the difference between the employment rates of men and women for each country. The countries are ordered by the size of the difference in employment rates, with those having the largest differences at the top of the chart.

To improve readability, I set the y-axis to show the countries, with a dash line grid. I also added a title and subtitle to the chart, as well as a caption to cite the data source. Finally, I colored the dots representing men and women differently and included a legend on the bottom of the chart to explain the colors.

I spent a lot of time creating this chart, especially on formatting it properly. During the process, I consulted multiple sources to ensure that the chart was clear and informative.

|Article|Details|
|-------|-------|
|Topic|Women’s employment in the EU|
|Publication date|	6/3/2020|
|Link|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/EDN-20200306-1?inheritRedirect=true&redirect=%2Feurostat%2Fnews%2Fwhats-new|
|Data|Eurostat’s database: [Employment and activity by sex and age - annual data](https://ec.europa.eu/eurostat/databrowser/view/LFSI_EMP_A$DV_881/default/table?lang=en)|
|Variables|Employment rate,Geo,Sex|
|Reference |For more information on Gender Statistics, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Gender_pay_gap_statistics) and this [one](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Gender_statistics). For the dumbbell chart, I used various sources but mainly this [one](https://r-graph-gallery.com/web-extended-dumbbell-plot-ggplot2.html).

### Code & plot
<img width="539" alt="2" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/d102a1c6-186c-4230-aa7d-1bd55e24b588">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L55-L128).

## 3. Barchart with R base

### Code & plot
<img width="542" alt="3" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/4b4ef8aa-5238-4d2f-a340-756f61aaf5d1">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L132-L154).

## 4. Line chart with R Base plot
<img width="491" alt="4" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/96a4bd9d-cf19-4f79-ad01-2dd5c5b1a602">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L158-L187).

## 5. Small multiples pie charts with ggplot2

### Code & plot
<img width="310" alt="5" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/aa53f397-c49b-4fc8-ba9d-a7837631826d">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L190-L233).

## 6. Stacked bar chart with ggplot

### Code & plot
<img width="504" alt="6" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/b8a14966-ddfb-438c-919f-42a0533a6414">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L235-L278).

## 7. 100% stacked barchart with ggplot2

### Code & plot
<img width="475" alt="7" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/3cb97fd8-00cb-4799-b8ea-f9e92d55ccd9">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L282-L311).

## 8. Scatterplot

### Code & plot
<img width="509" alt="8" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/784d4d82-2f4c-4c3c-9014-fea928398256">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L314-L330).

## 9. Treemap

### Code & plot
<img width="502" alt="9" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/4cb54de0-52f6-44e0-bf4d-09cd0c3bf0d5">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L334-L351).

## 10. Horizontal barplot

### Code & plot
<img width="513" alt="10" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/cad87b2c-8530-40d9-9b1f-b5951bbda688">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L354-L375).


