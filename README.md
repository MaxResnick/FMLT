# Forcasting Global Labor Market Trends Using Recurrent Neural Networks. 
### Max Resnick

### Acknowledgements:
Thanks to Haishan Yang, William Hardson, Umut Acikel, and Anupam Upadhyay. For assisting with the first iteration of this project which was first inteded for a UN competition. That version is available at https://colab.research.google.com/drive/1RpQGlfvw1KL_CmZE0TDXUjH5q0V81O5H#scrollTo=cuXc_yViG5-T
###Introduction
Welcome to the next generation of labor market forcasting models. Our aproach is unique in that, instead of merely using historical data, we use another data source: frequency of patent filings. In theory, the frequency of patent filings will allow us to predict points of rapid inflection which would not otherwise be detectable in the data. 
###Literature Review
Labor force projections are important references for policy making. Since 1915, the U.S. Bureau of Labor Statistics (BLS) has been publishing a journal, the Monthly Labor Review, which contains labor statistics and projections. (U.S. Bureau of Labor Statistics).

The standard labor projections apply econometrics and time-series models. In these models, the labor participation rate depends on several major components: labor force, aggregate economy, industry final demand, occupational employment, industry employment and industry output. However, over the years, the projections from BLS constantly underestimate the real trend because other trends such as economic growth, population dynamics and change in occupational employment, due to technological advancements are often unpredictable. For example, increasing life expectancy has caused people to stay in the labor force longer. The immigration is also important in the dynamics of the labor force. (Saunders, 2005)

There are other approaches employed by BLS such as cohort approaches and behavior approaches. The former strategy is to follow a representative cohort closely for a period of time. Then based on the data collected from this cohort, the BLS predicts the change in a larger population. The later approach has been at the center of much labor economics research for two decades. It studies the relationship between the socioeconomic characteristics and the labor supply. One example of this research is to study income and substitution effects in the labor market (Franklin, 2007).

Recently, there are a growing number of forecasting models using Artificial Neural Networks (ANN), which allow complex non-linear relationships between the response variable and its predictors (Hyndman and Athanasopoulos,2014). Using panel data of 439 German regions, Patuelli et al (2006) evaluated the performance of ANN models as forecasting tools for regional employment growth. Al-Zwainy et al (2012) built a model based on ANN to predict the productivity of finishing marble works for floors. They found that the model had an ability to predict the productivity for finishing works with a very good degree of accuracy. The coefficient of correlation was 89.55% and average accuracy percentage of 90.9%. 


###Data Sources

There are two primary data sources: geocoded patent data and ILOSTAT Labor trends data. The geocoded patent data was gathered from(Rassenfosse, Kozak, and Seliger 2014), published in Nature. We also gathered data from multiple soureces on Country specific GDP, Population, and Inflation. 

The geocoded patent data is primarily for the priority/first filings, the documents that first describe the invention. We used the geocoded patent data recorded by country of the inventor rather that by country of the applicant since the former has over 600,000 more observations which are not present in the latter. The geocoded patent data (by country of inventor) is for 54 named countries from year 1980 to 2014. As additional predictors, we used country specific annual figures for total GDP, inflation and population.


