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
For the third visualization, I recreated the chart from section 2, but this time using R base to create a bar chart. Since the details of the data and purpose of the chart are the same, I will only provide the code and the plot.

To create the chart, I used the same dataset as in section 2 and used data wrangling to assign different colors to the EU average to be easily compared with the rest of the countries. Then, I used the R base plot function to create the bar chart. The chart shows the employment rate of women and men in the EU for 2018, with the countries listed on the x-axis and the employment rate on the y-axis.

To make the chart more readable, I set the background color to white and adjusted the margins. I added a title to the chart and included a unit of measurement in the y-axis label. I also used different colors for the bars representing women and men and added a legend to explain the colors.

### Code & plot
<img width="542" alt="3" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/4b4ef8aa-5238-4d2f-a340-756f61aaf5d1">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L132-L154).

## 4. Line chart with R Base plot
For my fourth visualization, I recreated a graph from an article about EU citizens who died from influenza. The data I used was downloaded from Eurostat's website and saved as an Excel file on my local drive. The variables I focused on were the cause of death standardized death rate, countries, and age group. Since the article focused on trend analysis, I decided to recreate the original visual.

To create the graph, I used the R base plot function and adjusted the margins and background color to a dark blue. The graph shows the standardized rate of deaths from influenza by age group in the EU, with years listed on the x-axis and the death rate on the y-axis.

To make the graph more readable, I removed the box around the plot area and added white lines and labels to the axis. I also added a title and subtitle to the graph and used different colors for the lines representing the death rate for those under 65 years old and those aged 65 or over.

|Article|Details|
|-------|-------|
|Topic|EU citizens who died from influenza|
|Publication date|7/4/2020|
|Link|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/DDN-20200407-1|
|Data|Eurostat's database: [Causes of death - standardised death rate by NUTS 2 region of residence](https://ec.europa.eu/eurostat/databrowser/view/HLTH_CD_ASDR2__custom_6895314/default/table?lang=en)|
|Variables|Causes of death - standardised death rate,Age group,Time|
|Reference|For more information on health statistics, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Health_statistics_introduced).

### Code & plot
<img width="491" alt="4" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/96a4bd9d-cf19-4f79-ad01-2dd5c5b1a602">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L158-L187).

## 5. Small multiples pie charts with ggplot2
For this visualization, I used small multiple pie charts to display the proportion of primary to upper secondary education teachers in each country of the EU, categorized by sex. This format was chosen to allow viewers to easily compare the proportion of male and female teachers across different countries, while the charts were arranged in a grid to facilitate this comparison. The data used in this project was obtained from Eurostat's website and saved as an Excel file on my local drive.

To create the small multiple pie charts, I used the ggplot2 package in R. The size of each pie chart is consistent, which makes it easy to compare the proportion of male and female teachers across different countries. I customized the plot by adding a title, subtitle, and caption, adjusting the color scheme, and formatting the legend and background. However, one challenge I faced was adding labels to the pie charts, which was something I could not figure out how to do.

To prepare the data for the visualization, I performed data wrangling to convert the data into a format that could be used to create the pie charts. The ggplot2 package was then used to create the basic pie charts, which were transformed into polar coordinates to create the circular shape. Despite the labeling challenge, the resulting visualization effectively presents the proportion of male and female teachers in each country of the EU in an accessible and engaging way, thanks to the use of small multiple pie charts.

|Article|Details|
|-------|-------|
|Topic|Teachers in the EU|
|Publication date|5/10/2020|
|Link|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/edn-20201005-1|
|Data| Eurostat's database:[Classroom teachers and academic staff by education level, programme orientation, sex and age groups](https://ec.europa.eu/eurostat/databrowser/view/EDUC_UOE_PERP01__custom_6895421/default/table?lang=en)|
|Variables|Primary to upper secondary teachers,Geo,Sex|
|Reference|For more information on education and training, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Education_and_training).|

### Code & plot
<img width="310" alt="5" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/aa53f397-c49b-4fc8-ba9d-a7837631826d">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L190-L233).

## 6. Stacked bar chart with ggplot
In this visualization, I recreated the [third graph](https://ec.europa.eu/eurostat/documents/4187653/10321620/School+teachers+by+age.jpg/) from the [article](https://ec.europa.eu/eurostat/web/products-eurostat-news/-/edn-20201005-1) also presented in section 5. Since the details are the same as in section 5, I am going to present the code and the plot.

The original visual shows the proportion of primary to upper secondary education teachers in each EU country, grouped by age. To create the plot, I used ggplot2 and imported the data from Eurostat's website .I converted the country variable into a factor and used the gather function to transform the data into a long format. I also multiplied the proportion of teachers by 100 to show it as a percentage.

The resulting plot displays the proportion of teachers in each EU country, grouped by age, with each age group represented by a different color. The bars are stacked on top of each other, and the y-axis shows the percentage of teachers in each age group. To enhance the visual appeal of the graph, I used the scale_fill_manual function and Adobe color palette to customize the color scheme. I also customized the plot's title, subtitle, caption, and legend using ggplot2's theme function.

### Code & plot
<img width="504" alt="6" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/b8a14966-ddfb-438c-919f-42a0533a6414">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L235-L278).

## 7. 100% stacked barchart with ggplot2
For the seventh visualization, I recreated a graph from Eurostat’s website using a stacked bar chart in ggplot2 (less fancier thought). The chart shows the distribution of adults in households with young children according to their working patterns and the number of children and age of the youngest child.

I downloaded the data from Eurostat’s website and saved it as an Excel file on my local drive. Using ggplot2, I transformed the data into a long format using the gather function and customized the chart’s title, subtitle, caption, and legend. I also used a customized color scheme using the scale_fill_manual function. Overall, this visualization provides an informative and visually appealing way to compare the proportion of adults in households with young children based on their working patterns and family size using a stacked bar chart.

|Article|Details|
|-------|-------|
|Topic|Working parents with young children in the EU|
|Publication date	|1/5/2020|
|Link|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/DDN-20200501-1
|Data|	Eurostat’s database: [Number of adults by working status within households, number of children and age of youngest child](https://ec.europa.eu/eurostat/databrowser/bookmark/0b7dd284-cfaf-4a6b-adb3-56af1cb3c2ee?lang=en)|
|Variables|adults by working status within households, number of children and age of youngest child
type of household|
|Reference|Non applicable|

### Code & plot
<img width="475" alt="7" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/3cb97fd8-00cb-4799-b8ea-f9e92d55ccd9">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L282-L311).

## 8. Scatterplot
I got the idea to analyze the relationship between the duration of working life and GDP per capita while working on an article about working life. Although not identical to the article, it inspired me to plot the data in a scatterplot. The plot shows that countries with longer working lives generally have higher GDP per capita, indicating better opportunities for education and training, higher innovation levels, and more flexible labor markets. However, there are two exceptions: Ireland and Luxembourg, which have shorter working lives but the highest GDP per capita in 2018.

The plot was created using the ggplot2 package in R and displays each country as a point on a chart with the x-axis representing GDP per capita and the y-axis representing working life duration. Country labels were added using the geom_text_repel function, and the y-axis was customized using breaks and limits. The chart was given a light theme, and a red point was added to highlight the position of the countries.  

|Article|Details|
|-------|-------|
|Topic|Duration of working life on the decline in 2020|
|Publication date|1/7/2021|
|Link|[Duration of working life on the decline in 2020 - Products Eurostat News - Eurostat (europa.eu)](https://ec.europa.eu/eurostat/web/products-eurostat-news/-/ddn-20210701-1)|
|Data|Eurostat’s database: [duration of working life](https://ec.europa.eu/eurostat/databrowser/view/lfsi_dwl_a/default/table?lang=en) and [GDP per capita](https://ec.europa.eu/eurostat/databrowser/view/sdg_08_10/default/table)|
|Variables|Working years,GDP per capita,Geo|
|Reference|For more information on duration of working life, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Duration_of_working_life_-_statistics).For more information on GDP, visit this [link](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=GDP_per_capita,_consumption_per_capita_and_price_level_indices).

### Code & plot
<img width="509" alt="8" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/784d4d82-2f4c-4c3c-9014-fea928398256">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L314-L330).

## 9. Treemap
For this visual I also used the ggplot2 and treemapify packages to create a treemap that presents the share of own account workers in the EU by economic activity. Each box in the chart represents an economic activity, and a red point was added to highlight the position of the countries. The data was downloaded from Eurostat’s database on self-employment by sex, age, and economic activity. The treemap was colored using the viridis_c option in the scale_fill function. The figures were collected through the EU Labour Force Survey.

|Article|Details|
|-------|-------|
|Topic|Own-account workers in the EU|
|Publication date	|15/6/2020|
|Link|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/ddn-20200615-1|
|Data|Eurostat’s database: [Self-employment by sex, age and economic activity](https://ec.europa.eu/eurostat/databrowser/bookmark/0055e14c-bb6d-4e54-a7f0-2448b5ab752a?lang=en)
|Variables|Own account workers by economic activity|
|Reference|The figures were collected through the [EU Labour Force Survey](http://ec.europa.eu/eurostat/web/lfs)|

### Code & plot
<img width="502" alt="9" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/4cb54de0-52f6-44e0-bf4d-09cd0c3bf0d5">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L334-L351).

## 10. Horizontal barplot
I used R’s barplot() function to create a horizontal chart presenting the old-age dependency ratio - the ratio of elderly people (65+) to working-age individuals (15-64). Eurostat projects that the EU’s ratio will double to 57% by 2100, meaning there will be less than two working-age individuals per elderly person. I customized the plot with bar color, border, and y-axis label using col and mtext(). The main title and subtitle were added with title(), using col.main and col.sub to set the text color. I modified the x-axis with axis() and added vertical gridlines with abline().

|Article|Details|
|-------|-------|
|Topic|Old-age dependency ratio increasing in the EU|
|Publication date|13/7/2020|
|Link|https://ec.europa.eu/eurostat/web/products-eurostat-news/-/DDN-20200713-1?inheritRedirect=true&redirect=%2Feurostat%2Fnews%2Fwhats-new|
|Data|Eurostat’s database: [Projected old-age dependency ratio](https://ec.europa.eu/eurostat/databrowser/view/tps00200/default/bar?Lang=en)|
|Variables|Projected old-age dependency ratio,Geo|
|Reference|Non applicable|	

### Code & plot
<img width="513" alt="10" src="https://github.com/ZoiDiama/My-tidytuesday-projects/assets/139105670/cad87b2c-8530-40d9-9b1f-b5951bbda688">

Check the code [here](https://github.com/ZoiDiama/Plots-for-Eurostat-data-with-R/blob/1f8a8dc1e1f2a93829651d7e78dbe055214985a4/Code/all_visuals#L354-L375).


