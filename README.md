# Live Project

## Introduction
For the final two weeks at The Tech Academy, I worked on several mock stories simulating the life of a data scientist. Doing these mock stories was a great learning opportunity for visualizing data, cleaning data, grouping data, and parsing csv files. There were many obstacles that I had to navigate through, but ultimately delivered high quality work in a timely manner. I worked on several csv files that I am very proud of, such as [Google Play Store](#google-play-store), [COVID-19](#covid-19), and a little bit of the [NBA](#nba). The programs that I used for these stories were Jupyter Notebook, and Power BI. Over the two week sprint we used the Agile/Scrum method. We had daily standups and a code retrospective at the end of each week. Although I worked on these stories alone I was a part of a team of other software developers. We all met up at the daily standup and got insight on what everyone was working on. I am confident I will be using these skills and some other [skills](#other-skills-learned) in the future.
  
Below are descriptions of the stories I worked on as well as some code snippets and data visualizations.


## Google Play Store
* [App Count Per Category](#app-count-per-category)
* [App Rating Correlation](#app-rating-correlation)



### App Count Per Category
This story was a particularly easy one where I needed to find the total number of apps in three specific categories on the Google Play Store. The data given to me had a total of 10,841 apps. In order to find the total of each caetgory I first separated my data into a new data frame with only those 3 categories. 

![Count plot categories GPS](https://user-images.githubusercontent.com/93669845/152563363-9d40d9be-fa82-4b97-93bc-3bfe913b9e48.png)

I also needed to find the total count of free apps and paid apps so I made a data frame for the free apps and a data frame for the paid apps. I also made countplots of both of those giving me the total number of free apps and the total number of paid apps. 

![free_paid GPs](https://user-images.githubusercontent.com/93669845/152564234-52eacb7c-e5e1-4183-8f6e-9323d70c6c41.png)

### App Rating Correlation
For this story I needed to find a correlation between the total number of installs and the rating of the app. We were looking to see if the rating of the app had any correlation to the app being installed. In order to find the correlation I had a lot of data cleaning to do. I needed to find the total sum of installs per rating, but the install column was filled with '+' symbols (i.e. 1000+). I removed all of the plus signs and converted the column into an integer column in order to get the sum later. 

![replace](https://user-images.githubusercontent.com/93669845/152565595-2a813054-d557-474f-84ac-5bc0c4825360.png)

Once that was complete I separated my data into their own data frames by rating. I would drop all columns but the Install and get the total sum. With my data frame now only being the content rating and its respective sum. I needed to concat all of my data frames together to compare them to each other on a graph (I realize now after that I could have grouped the data frame by content rating and got the sum that way as well). I found the correlation by using the correlation function built into Jupyter Notebook.

![Correlation](https://user-images.githubusercontent.com/93669845/152567215-37d771d3-8ff5-483f-b093-aaac14532779.png)

*Jump to: [NBA](#nba), [Skills](#other-skills-learned), [Page Top](#live-project)*

## COVID-19
* [Average new cases](#average-new-cases)
* [Severity](#severity)
* [Now vs Then](#now-vs-then)


 
### Average New Cases
In this story I needed to find the average new cases in each country. I was given a data set that held 121,034 rows and 65 columns. Within those rows there were 225 countries and 6 continents. In order to find the average new cases I needed to do some grouping. I grouped my data by location making 2 separate data frames. In the first I found the count of total new cases in each country, and in the second I found the total sum of new cases in each country. I then made another new data frame that divided the total sum by the count of new cases, giving my new data frame the average number of new cases in each country. When that was all done I saved my data as a csv file and swapped over to Power BI. I displayed the average number of new cases in each country by separating them by continent.

![Average new cases](https://user-images.githubusercontent.com/93669845/152570685-48c157a0-14c3-481b-85b7-2a67c1071877.png)

### Severity
This story wanted the severity of covid in each country. I took into consideration the amount of deaths, ICU patients, hospital patients, and total population. I created two separate data frames both grouped by location and continent. In the first I needed the sum of the ICU patients, and hospital patients. and in the second I wanted the last record of total deaths and toal new cases. I realized very quickly that I had outliers again because the population plays such a huge factor in trying to compare total cases. So I had to divide my columns by the country's total population in order to get graphs to accurately represent the severity. I merged both of those data frames giving me one data frame that was ready for the program Power BI.

![Death by Case](https://user-images.githubusercontent.com/93669845/152573332-7645abbe-e408-4fd3-9e99-0a7a0fc0bd5b.png)
![ICU Population Percent](https://user-images.githubusercontent.com/93669845/152573347-dcd4ea46-b3c5-4d73-a8ab-d7e117e56532.png)

### Now vs Then
I was tasked with comparing how the countries were responding to covid over the past two years. I made line charts in Power BI to show the spikes and valleys with new cases over the course of 2020, and 2021. I grouped them all by continent to see who responded the best and worst in each continent. Here is an example of Europe. I'm using Europe as an example because this shows the most dynamic countries and I didn't have to play around outliers with this graph either.

![2020](https://user-images.githubusercontent.com/93669845/152575584-86f4c957-a9b3-4349-81f9-a0d9e1c6553c.png)
![2021](https://user-images.githubusercontent.com/93669845/152575594-40f71da1-af0f-4850-aba7-f0dbcfaadb8d.png)

*Jump to: [Google Play Store](#google-play-store), [Skills](#other-skills-learned), [Page Top](#live-project)*

## NBA
[Age vs Production](#age-vs-production)


### Age vs Production
In this final story I was tasked with finding when players reach their peak. This story was probably my biggest hurdle because I know very little of the NBA. All of the columns were abbreviations of NBA terms, soa after some googling I was finally ready to start looking at my data. I created more line charts on Power BI with this story as well because I wanted to track their stats based on how long they played for. So I took the top 10 players that had the most games played and compared how many years they were playing for with their stats (i.e. 3 Points attempted, Free throws made, etc.)

![NBA](https://user-images.githubusercontent.com/93669845/152577909-a1d66050-6daa-4367-96bb-f195db1f4b0e.png)

*Jump to: [Google Play Store](#google-play-store), [COVID-19](#covid-19), [Page Top](#live-project)*

## Other Skills Learned

* Learning new efficiencies from other developers by observing their workflow and asking questions
* Working as a team
* Efficiently use Jupyter Notebook and Power BI
* Working on a project alone
