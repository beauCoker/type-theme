---
layout: post
title: Duke Data Visualization Workshop
---

Last week I participated in a workshop with the Duke Data and Visualization Services Department. One of our tasks was to take an existing dataset and improve a made-up chart. 

To be clear, the data from the National Ocean Service of the National
Oceanic and Atmospheric Administration (NOAA) is real [(avaiable here)](https://products.coastalscience.noaa.gov/rea/data_By_StudyID/nutrient_data_by_studyid.aspx?study=44), but the chart is made-up for the workshop and is designed to be awful. Here it is, which shows observed chemical concentrations at a North Carolina creek over a two day period: 

![Before chart](/img/2016-10-08-duke-data-visualization/original.png)

This chart is filled with problems, including:
*	3D shapes that confer no additional information
*	Confusing labels
*	Different scales (measurements are actually repeated in different units)
*	Time on the vertical axis
*	No axes labels

I could go on, but the chart was so awful that I thought it best to scrap it and start from the begining. Here's what I came up with:

![After chart](/img/2016-10-08-duke-data-visualization/nerrs.png)

Now, the first thing to note about this chart is that there is a great deal more data shown. Instead of showing a single site over two days, I grouped all eighteen sites into four geographic locations and showed the average observation over time for each group. The inset chart in the lower-right shows the four location groups (the latitude and longitude are real but the direction is made-up for illustration).

The original idea was to create a parallel coordinates plot for these four groups. However, noticing that these groups were approximately arranged in a line, I projected each group's location (average over sites) onto the OLS line and used this distance to stretch the parallel coordinates plot horizontally. I think it creates a neat effect. For example, you can see that while Zekes Island and Masonboro are close geographically, their chemical concentrations tend to change by nearly as much as between Masonboro and Rachel Carson, which are much further part. 

Overall this chart is a little messy, and the colors aren't greeat (especially the yellow), but it's an improvement. 
