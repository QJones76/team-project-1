# team-project-1
In this project, we took a crime dataset for all crimes in Chicago from 2001 to Oct. 25, 2024. We cleaned and processed the dataset to a manageable csv file. Our analysis focused on trying to find how crimes were affected by the pandemic. We defined the pandemic as starting from [Jan 31, 2020](https://www.cdc.gov/museum/timeline/covid19.html#:~:text=January%2031%2C%202020&text=The%20Secretary%20of%20the%20Department,outbreak%20a%20public%20health%20emergency.) and ending on [May 11, 2023](https://www.pfizer.com/news/announcements/global-and-us-agencies-declare-end-covid-19-emergency#:~:text=On%20May%205%2C%20more%20than,PHE%20for%20COVID%2D19.).

---

### Preparing the Data
We got our dataset from the [data.gov](https://data.gov/), which gave us the Chicago crime dataset found [here](https://catalog.data.gov/dataset/crimes-2001-to-present). Furthermore, [here](https://drive.google.com/drive/folders/1ZCfgfvfEzVo_4WvWrI68Wil6KQ-bgP5C?usp=drive_link) is a link with our large csv files. 

###### Step 1: Filtering down the data
We started by filtering out all rows that don't fit in our time frame. We wanted at least the same amount of data before the pandemic in coparision to the duration of the pandemic. Roughly, we were looking at least 3 years before the pandemic. Thus we filtered out all rows before 2016 and exported it to a filtered csv file

###### Step 2: Cleaning the data
We then took our filtered data set and removed about 31,000 rows containing null values. While that might seem like a lot, it was only about 1.5% of our dataset. We also filled in 7800 null values in a single column with the word "Unknown" due to the fact that the column is an extra descriptor of another column. At the end of this porcess, we have a cleaned dataset that we then exported to a csv file for analysis. 

---

### Our Analysis

- Was crime affected by the pandemic?
    - Crime went down during the beginning pandemic. We can see this in the 'Yearly_Crime_Incidents' chart which shows that crime went down by over 50,000 total incidents in the year 2020. Furthermore, in 2021 the toal incident count dropped about 3,000 more than the year before. It is only in 2022 that we see crime start to return to pre-pandemic numbers.
    - We can see this being futher demonstrated by the 'Incident_Counts_by_Pandemic_Period' chart which shows almost 100,000 less cases during the pandemic period than before, and the after pandemic period, which is a little less than half the same amount of time for the other time periods, has about half of what the pre-pandemic period has. This means that crime is increasing again because it has roughly half the amount of incidents with half the amount of time. However, more analysis would need to be done to actually predict if cime will reach pre-pandemic numbers. 
- Did seasons affect crimes in Chicago?
    - When analyzing the monthly crime incidents over the entire time period, we notice these consistent bumps in the data. The way the bumps were positions in the data made us think that there is a seasonality component that effects when crime is commited.
    - This is proven with the Seasonality_Component chart. There is a slight increase in total for crimes in the summer and a slight decrease in total crimes commited in the winter.
 - Did arrest rates get altered over the course of the pandemic?
    - Another component of crime is the arrest rates. We noticed that the number of arrests went down significantly since the pandemic. We can see this in the "Arrests_Over_Time" chart.
    - Furthermore, arrests went down across all the major categories of crime.
    - While crime seems to be on the rise after the pandemic period, arrest have remained more stagnant  
- Did the pandemic have a geolocation effect to where crime occures in the city? 
    - While ultimately, crime did go down, it doesn't seem like the pandemic affected the geolocation of where crimes will occur in the city. We can see this demonstrated in the charts named "Chicago_All_Crimes_Hotspots_Before_Pandemic" and "Chicago_All_Crimes_Hotspots_During_Pandemic" found in the Data_viz_output folder. The hotspots still clump together in the same general area. 
    - Furthermore, we can look at the "Chicago_All_Crimes_Hotspots_During_Pandemic" chart and see that the same clumping patterns appear even with a smaller time frame. 

### Final Conclusions
Ultimatly, crime was affected by the pandemic, and while our analysis scratched the surface of interpretable outcomes, we still think that there could be a lot more done to find more concrete results of the exact factors of the pandemic that affected crime in the city of Chicago. 


### Citaitons that Helped with Coding
- [This](https://pandas.pydata.org/docs/reference/api/pandas.cut.html) was used to find out about more pandas cut function. 
- [This](https://stackoverflow.com/questions/1549641/how-can-i-capitalize-the-first-letter-of-each-word-in-a-string) was used to find out how to capitalize the first letter of a string only in python
- We used all three of these matplotlib documentation: [matplotlib.pyplot.subplots](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.subplots.html), [Separate calculation and plotting of boxplots](https://matplotlib.org/stable/gallery/statistics/bxp.html#sphx-glr-gallery-statistics-bxp-py), and [matplotlib.axes.Axes.bxp](https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.bxp.html#matplotlib.axes.Axes.bxp), as well as, [Chat GPT](https://chatgpt.com/) to both understand how to create and display boxplots on the datasets time periods.
- [W3schools](https://www.w3schools.com/python/ref_func_zip.asp) and the [Python documentation](https://docs.python.org/3/library/functions.html#zip) in association with [Chat GPT](https://chatgpt.com/) were all used to figure out how to correctly implement the zip function in python for our plotting loops.
- [This](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.legend.html) in association with [Chat GPT](https://chatgpt.com/) was used to help us position our chart's legends in a more readable position.
- We used [W3schools](https://www.w3schools.com/python/ref_set_intersection.asp) in association with [Chat GPT](https://chatgpt.com/) to understand how set and intersection can work to find similar values across sets.
- In a similar fashion, we used [W3schools](https://www.w3schools.com/python/ref_set_union.asp) to understand how set and union can work to find unique values across sets. 
- We used [this](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.transform.html) in association with [Chat GPT](https://chatgpt.com/) to transform and count values in our datframes for later plotting

 

