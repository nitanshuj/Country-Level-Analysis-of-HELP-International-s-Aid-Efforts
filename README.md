# Mini Project 3 - HELP International - Priority Country List for Humanitarian Aid

----------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------

This was a Mini-Project, I completed as a part of my Post Graduate Diploma in Data Science from Upgrad & IIIT-Bangalore. The dataset and the Problem Statement was provided to me by Upgrad.

`The report that follows is my explanation of what was performed in the Mini-Project.`

----------------------------------------------------------------------------------------------------------------

## Business Understanding
----------------------------------------------------------------------------------------------------------------
HELP International is an international humanitarian NGO that is committed to fighting poverty and providing the people of backward countries with basic amenities and relief during the time of disasters and natural calamities. It runs a lot of operational projects from time to time along with advocacy drives to raise awareness as well as for funding purposes.

After the recent funding programs, they have been able to raise around $ 10 million. Now the CEO of the NGO needs to decide how to use this money strategically and effectively. The significant issues that come while making this decision are mostly related to choosing the countries that are in the direst need of aid. 

----------------------------------------------------------------------------------------------------------------
 
## Business Objective
----------------------------------------------------------------------------------------------------------------
The objective of this mini-project us to categorize the countries using some socio-economic and health factors that determine the overall development of the country. Then you need to suggest the countries which the CEO needs to focus on the most.

----------------------------------------------------------------------------------------------------------------

## Data Dictionary
----------------------------------------------------------------------------------------------------------------

| Column Name |   Description  |
| :- | :------------- |
| **country** |	Name of the country |
| **child_mort** | Death of children under 5 years of age per 1000 live births |
| **exports** | Exports of goods and services per capita. Given as %age of the GDP per capita |
| **health** | Total health spending per capita. Given as %age of GDP per capita |
| **imports** | Imports of goods and services per capita. Given as %age of the GDP per capita |
| **Income** | Net income per person|
| **Inflation** | measurement of the annual growth rate of the GDP deflator |
| **life_expec** | The average number of years a new born child would live if the current mortality patterns are to remain the same |
| **total_fer** | The number of children that would be born to each woman if the current age-fertility rates remain the same. |
| **gdpp** | The GDP per capita. Calculated as the Total GDP divided by the total population. |

----------------------------------------------------------------------------------------------------------------

## Methodology
----------------------------------------------------------------------------------------------------------------

- 1- Reading and getting basic understanding of the Data
- 2- Data Quality Check & EDA
- 3- Outlier Analysis
- 4- Checking Cluster Tendency (Hopkin's Test)
- 5- Data Preparation for Modelling - Re-scaling [Standard Scaling]
- 6- Choosing the Best value of K
    	- a. SSD
	- b. Silhouette's Analysis
- 7- Model Building
   	- a. K-Means Clustering Model
       		- i. Make the Model
       		- ii. Visualize the clusters using scatter plot and boxplots
		- iii. Perform Cluster Profiling (gdpp, child_mort, income)
   	- b. Hierarchical Clustering Model
       		- i. Make the model
       		- ii. Single Linkage with Dendrogram
       		- iii. Complete Linkage with Dendrogram
       		- iv. Use suitable method and perform the final cut.
       		- v. Visualize the clusters using scatter plot and boxplots.
      		- vi. Perform Cluster Profiling (gdpp, child_mort, income)
- 8- Using both the results and reporting countries that are in need of the aid.

----------------------------------------------------------------------------------------------------------------

## Observations and Inferences from the Data Plotting and Visualization:
----------------------------------------------------------------------------------------------------------------

- It was observed that all the variables except life_expec shows right-skewed behavior on the distplot.
- life_expec on the other hand shows left-skewed behavior.
- It can be inferred that life expectancy is high for most of the countries.
- Also, the other remaining columns - 'income', 'total_fer', 'gdpp', 'child_mort', 'inflation', 'imports', 'exports' and 'health' gives an inference that most of the countries have low values of the these.
<br><br><br>

#### Bivariate Analysis

- Total Fertility vs Child Mortality <br>
  We see that the relationship follows a near linear relationship. We see that as the Total Fertiliy rates for a 
  country increases, the child mortality rates also increases.
<br><br>
- Income vs GDPP <br>
  This also follows a linear trend. We can say that a country with high GDPP will also have a higher Net income.
<br><br>
- Income vs Inflation<br>
  We don't observe a linear relationship between income and inflation. 
<br><br>
- Import vs Exports<br>
  Import and exports shows a strong linear relationship. We can say that higher the number of imports, higher
  will be the number of exports for a country.
<br><br>
- Life Expectancy vs Health Expenditure<br>
  We cannot observe a linear pattern between them. But we can say that if the health expenditure increases, 
  there is a high chance of life expectancy increasing too.
<br><br>
- Life Expectancy vs GDPP<br>
  It is similar to the previous case. We cannot observe a linear pattern between them. 
  But we can say that if the gdpp increases, there is a high chance of life expectancy increasing too.
<br><br>
- Income vs Health Expenditure<br>
  We can say that countries with high income tend to spend more on health expenditure.
<br><br><br>

#### Observations from the Heatmap
- We observe that there is pretty high positive or negative correlation between most of the variables.
- But, since Clustering is not affected much by collinearity, thus we will ignore the collinearity between the variables for this case.
- Hence no change or treatment of data is required here.
<br><br><br>

----------------------------------------------------------------------------------------------------------------

## Conclusion & Business Insights
----------------------------------------------------------------------------------------------------------------

I made the use of Clustering techniques for this particular problem.<br>
I used two types of clustering models for this mini-project - 
- K-Means Clustering
- Hierarchical Clustering

It was observed that both the methods gave identical results. It was also found that K-Means generated a cluster of 45 countries and Hierarchical generated a cluster of 47 countries. 

So we can said that both the algorithms gave optimal results, although we had to take 3 clusters in K-means compared to 4 clusters in Hierarchical clustering. Both the choice of choosing number of clusters were verified using Silhouette's Score and not much difference was observed in choosing 3 clusters or 4 clusters.

We can now suggest the CEO of HELP International that the top 20 countries that are in dire need of aid are -
- 1 - Burundi
- 2 - Liberia
- 3 - Congo, Dem. Rep.
- 4 - Niger
- 5 - Sierra Leone
- 6 - Madagascar
- 7 - Mozambique
- 8 - Central African Republic
- 9 - Malawi
- 10 - Eritrea
- 11 - Togo
- 12 - Guinea-Bissau
- 13 - Afghanistan
- 14 - Gambia
- 15 - Rwanda
- 16 - Burkina Faso
- 17 - Uganda
- 18 - Guinea
- 19 - Haiti
- 20 - Tanzania

----------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------














