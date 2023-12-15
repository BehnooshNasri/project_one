# Project One - Dream Team!
## Post-graduate Studies Enrollment and Graduation in Canada and Around the World 

## Installation and required packages
1. geopandas (installation may be required)
2. fiona (installation may be required)
3. pandas
4. matplotlib
5. os
 

## Description of the Project
This project uncovers some key factors relating to enrollment in post-graduate programs in Canada and around the world. It draws from census data and the data from the World Bank to present an analysis of these factors in the year 2020, focusing on data from four(4) selected Provinces in Canada (Ontario, British Columbia, Alberta and Quebec). Some variables considered are total population and GDP, in conjuntion with the following factors: 

- Total Income
- Gender
- Geographic Location

### The analysis we're going to do is:

1. Get data from different resources including StatCanada, Census, World Bank API, etc.
2. Cleaning the data and converting into dataframes
3. Merge different data frames to facilitate analysis
4. Analyze the data from different variables (income, gender, geographic location, etc.) to perform linear regression to find correlations
5. Anaylze the final data and prepare the presentation

### The questions we're going to answer are:

1. What is the distribution of household income and post-grad degrees in the select provinces of Ontario, British Columbia, Alberta and Quebec?
2. What is the different graduation rates for the select provinces of Ontario, British Columbia, Alberta and Quebec? 
3. What are the ratios between male and female graduates for post-grad studies in the select provinces of Ontario, British Columbia, Alberta and Quebec?
4. What are the countries with most international students enrolled in post-grad studies in Canada?
5. Using API, for available data globally, what are the post-grad statistics compared to the countries GDP?
6. Using API, for available data globally, what are the post-grad statistics compared to the countries population?


## Members of the group

The members in this group are:

1. Esi (@Esi-Akotia)
2. Sharvil (@sharvil-koonjul)
3. Amir (@Amirgol00)
4. Hamza (@malam300)
5. Behnoosh (@BehnooshNasri)

## Work breakdown strucutre

| Task     | Sub task   | Assigned to:   | Support:  |
| ------------- |-------------| :-----:|  :-----:|
| GitHub Setup | Main GitHub Host | Behnoosh |  |
|  | README file updates | Behnoosh, Esi | Amir, Hamza, Sharvil |
| Prepare Data | Retrieve datasets from StatCan | Amir, Sharvil | Esi |
| | Get data from APIs (REST Countries, World Bank) | Behnoosh, Hamza | Amir |
| | Clean Countries Population & GDP API data & save as csv | Behnoosh  |  |
| | Clean Income by Province data & save as csv  | Sharvil  |  |
| | Clean Gender data & save as csv  | Sharvil  |  |
| | Clean World Graduate data & save as csv  | Hamza  |  |
| | Clean Census Income & Enrollment data & save as csv  | Amir |  |
| | Clean Graduate data from Census Income & Enrollment data  | Esi |  |
| Analysis | Analyze Gender & Graduate data and plot graphs | Behnoosh   |    Amir, Esi, Hamza, Sharvil |
| | Analyze Country & Education data and plot graphs | Behnoosh   |    Amir, Esi, Hamza, Sharvil |
| | Analyze Income & Graduate data and plot graphs  | Esi   |    Amir, Behnoosh, Hamza, Sharvil |
| | Analyze Enrollment by Country data and plot graphs  | Sharvil   |    Amir, Behnoosh, Esi, Hamza |
| | Analyze World Enrollment data and plot heat maps  | Amir  |    Esi, Behnoosh, Hamza, Sharvil |
| Presentation | Set up Google Slides template | Esi |  |
| | Update slides with output from analysis | Amir, Behnoosh, Esi, Hamza, Sharvil |  |
| | Class presentation | Behnoosh, Esi | Amir, Hamza, Sharvil |

## Datasets used:

1. Census and StatCan: https://www12.statcan.gc.ca/census-recensement/index-eng.cfm
2. https://www12.statcan.gc.ca/census-recensement/2021/dp-pd/dt-td/Index-eng.cfm?LANG=E&SUB=98P1004&SR=0&RPP=10&SORT=releasedate
3. https://www12.statcan.gc.ca/census-recensement/2021/dp-pd/dt-td/Index-eng.cfm?LANG=E&SUB=98P1009&SR=0&RPP=10&SORT=releasedate
4. World Bank API: https://datahelpdesk.worldbank.org/knowledgebase/topics/125589-developer-information
5. REST Countries API: https://restcountries.com/#about-this-project-important-information
6. World Development Indicators | DataBank: https://databank.worldbank.org/reports.aspx?source=2&country=CAN#

## Code snippets
### creating the heat map for international students enrollment in post-grad studies in Canada for the year 2020

`fig, ax = plt.subplots(1, 1, figsize=(15, 10))
world.boundary.plot(ax=ax, linewidth=1)
merged_summed_data.plot(column='VALUE', ax=ax, legend=True,
                        legend_kwds={'label': "Number of Students"},
                        cmap='OrRd', alpha=0.9)
plt.title('Heatmap of International Students in Master\'s and Doctorate Programs in Canada by Country of Citizenship')
plt.savefig('Outputs/Heatmap_OGvalues_plot.png')

plt.show()`

## Analysis

### Behnoosh Analysis: 
1.	For gender based analysis: 
    a.	Ontario has the highest rate among the 4 for both female and male post grad students, Quebec is second, BC is third and Alberta is 4th. 
    b.	For all 4 provinces: Female population of post-grad for Masters and total highest certificate or degree is higher but it is slightly smaller for earned doctorates.
2.	For the world data based on GDP and Population: 
    a.	Country with the highest number of Masters degrees: Poland
    b.	Country with the highest number of Doctorate degrees: United States
    c.	Country with the lowest number of Masters degrees: Mozambique
    d.	Country with the lowest number of Doctorate degrees: Indonesia
    e.	For GDP vs post-grad data: it is not a very high correlation but there seems to be appositive one that with the bigger GDP of the available countries, the higher number of graduates. 
    f.	For population vs post grad data: three really isn’t a correlation for the data available for the countries. 
    
### Sharvil Analysis: 
1. For Master's or equivalent enrollments, we can see that the strongest countries with international students are China and India when comparing the two years. India had a higher increase in students in the second year in the comparison. We can see a slight increase in China, France and Iran as well.
2. For Doctoral or equivalent enrollments, China and Iran take the lead with the count of international students. Again, we can see an increase in students between the two. The number of students from Bangladesh also grew slightly while Egypt's dropped slightly.

### Hamza Analysis:
1. Poland and Estonia have outperformed globally in terms of the number of degrees achieved, considering both population and GDP.
2. Mozambique and Indonesia have recorded the lowest degree attainment.

### Esi Analysis: 
1. 

### Amir Analysis: 
1. Looking at the count and per capita analysis of the international student data, we have found countries such as Iran, China and India to be among the highest both in per capita and pure count values.

## Limitations

1.	For data collection: There is a limitation to World Bank API and I was unable to get the population of the countries from it so I had to use REST API. This resulted in a discrepancy in the name of some countries and as there wasn’t data in both, some countries were eliminated. 
2.	The education data for countries around the world is not comprehensive and we only were able to analyze only a few countries. Initially our plan was to compare countries similar to Canada’s population and GDP to post-grad education rates. However due to the lack of data available, we couldn’t achieve this, so we had to change our question to just compare education rates to each available country’s population and GDP. 
3.	The census data for male and female does not include people who do not identify as either gender. 
4.	We only focused on 4 provinces to analyze our data.    
5.	The main challenge was locating recent and reliable information, as many countries lacked data, especially for the year 2020.
6.	Finding a suitable API for world data that has the information we need.
7.	Adjusting our inquiries based on the insights gained from the data.
8.  The census data does not contain unique identifiers for individuals in their dataset. This posed as a challenge when comparing multiple datasets from this source.
9. Not enough data available to trace which income group is enrolling in post grad studies
10. Not enough data to determine which grad students are living in Canada vs those studying online




