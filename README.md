# Investigating Trends in In-Person and Online Physical Therapy from 2020 to 2025
## Introduction
Over the summer, I have been working as a receptionist at a physical therapy wellness center. While working, I questioned possible shifts in the trends of treatments due to the enhancement in technology and AI. 

This project will help to illustrate the current trends of in-person and online treatments and estimate the trends of patient behaviors in the near future. 

Going into the project, I expected that the number of in-person physical therapy visits would decrease and the number of online visits would increase due to the increasing use of technology.

I decided to split the experiment into two parts. I wanted to see what people are searching for online and if it had a correlation with actual behavior.
## Part 1: Online Search Trends
I initially started thinking that I wanted to use Google’s own API, but it was deprecated. As a result, I found another api that works similarly to Google’s. I used SerpApi to generate codes of data that provided the data sets of the numbers of in-person and online physical therapy in 2020 to 2025. With the code generated, I used Google Colab to use the code and form graphs that show trends of each over the years.

![Google Search Trends for In-Person Physical Therapy (2020-2024)](./Google%20Search%20Trends%20for%20In-Person%20Therapy.png)

![Virtual Physical Therapy Trend Line](./Virtual%20Physical%20Therapy%20Trend%20Line.png)
The graphs for both in-person and online trends all show an increase with a decreasing rate, meaning the rate at which the numbers of sessions are increasing is decreasing over time.
## Part 2: Insurance Data Trends
I went on Kaggle to find possible data sets I could use, but none showed up for the topic of online physical therapy. As a result, I went on Data.CMS.gov, which is used very commonly for academic research, where I searched for data sets that included data of in-person and online physical therapy. I wanted an actual insurance record so that the data I will be working with is true.

Because the data set I chose included various information from the service giver to individual types of treatments received which were all unnecessary, I had to go through a process of cleaning the data so that the information would narrow down the data. 

https://data.cms.gov/provider-summary-by-type-of-service/medicare-physician-other-practitioners/medicare-physician-other-practitioners-by-provider-and-service/data is where the data schema can be found; through some experimentation I decided to focus on 3 sections: Rndrng_Prvdr_Type, Tot_Bene_Day_Srvcs, Place_Of_Srvc. The data was also split into 5 separate files, one per year, so I added an additional column to represent the date when aggregating the data. In the end, I had a dataframe (spreadsheet) looked as follows: 

| Rndrng_Prvdr_Type | Tot_Bene_Day_Srvcs | Place_Of_Srvc |
| --- | --- | --- |
| Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3 |
| Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3 |

“O” stands for in-person data, and “F” stands for online data.

![In-Person Physical Therapy Trend Line](./In-Person%20Physical%20Therapy%20Trend%20Line.png)

![Virtual Physical Therapy Trend Line](./Virtual%20Physical%20Therapy%20Trend%20Line.png)
Part 2 shows a graph of both in-person and online moving in an upward direction. However, the slope or the rate of change for online physical therapy is higher. From the graphs, we can assume that as technology is advancing, more and more people will start to utilize virtual therapy. However, still compared to the numbers of in-person visits, the online one is far less, this shows that technology only recently started and began enhancing acceleratingly.
