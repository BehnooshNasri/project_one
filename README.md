# Project One - Dream Team!
## Post-graduate Studies Enrollment and Graduation in Canada and Around the World 

## Installation and required packages
1. geopandas (instalation may be required)
2. fiona (instalation may be required)
3. pandas
4. matplotlib
5. os
 

## Description of the Project
This project talks about what are some factors that can affect enrollment and graduation from post-graduate programs in Canada and around the world. 

Total Income;
Gender;
Geographic Location

### The analysis we're going to do is:

1. Get data from different resources including StatCanada and Census
2. Cleaning the data and converting into dataframes
3. Merge different data frames to start analyzing
4. Analyze the data from different variables (income, gender, geographic location, etc.) to perform linear regression to find correlations
5. Anaylze the final data and prepare the presentation

### The questions we're going to answer are:

1. What is the distribution of household income and post-grad degrees in select provinces of Ontario, British Columbia, Alberta and Quebec?
2. What is the different graduation rates for the select provinces of Ontario, British Columbia, Alberta and Quebec? 
3. What are the ratios between male and female graduates for post-grad studies in the select provinces of Ontario, British Columbia, Alberta and Quebec?
4. What are the countries with most international students enrolled in post-grad studies in Canada?
5. Using API, for abvialable data globally what are the post-grad statistics compared to the countries GDP?
6. Using API, for abvialable data globally what are the post-grad statistics compared to the countries population?


## Members of the group

The members in this group are:

1. Esi (@Esi-Akotia)
2. Sharvil (@sharvil-koonjul)
3. Amir (@Amirgol00)
4. Hamza (@malam300)
5. Behnoosh (@BehnooshNasri)

## Work breakdown strucutre

Task	Sub task	Assigned to:	Support:
Prepare Data	Get datasets from StatCan	Amir, Sharvil	Esi
"	Get data from API (REST API, World Bank API)	Behnoosh, Hamza	Amir
"	Clean data & save csv files	Amir, Sharvil	Esi
Analysis	Run statistical analysis	Behnoosh, Esi	Amir, Hamza, Sharvil
"	Create charts & graphs to show relationships	Behnoosh, Esi	Amir, Hamza, Sharvil
"	Report on key findings & draw conclusions	Behnoosh, Esi	Amir, Hamza, Sharvil
Presentation	Create powerpoint	Behnoosh, Esi, Hamza	Amir, Sharvil
"	Class presentation	Behnoosh, Esi	Amir, Hamza, Sharvil

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

## Limitations
