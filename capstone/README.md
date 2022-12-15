# Election Forecasting With Social Media Sentiment Analysis
## GA Capstone Project
The goal of this project is to use sentiment analysis of social media data in order to improve election predictions. The goal is not to build the best election forecasting model possible, but to show that social media data can be useful for forecasting elections. Any improvements

## Breakdown
* datasets folder containing processed datasets created during the poject
* polls folder containing polling data from [538](https://fivethirtyeight.com)
* images folder containing images used in the presentation
* social_media_data_collection.ipynb - Notebook that extracts text from social media
* election_model.ipynb - Notebook used to process data and build linear models
* EDA.ipynb - Notebook used for generating visualization

## Data
2022 polling data is from 538. Social media text is taken from reddit posts and comments containing the names of the candidates. I discoevered that other social media APIs were not suitable for the task required.

## Visualizations
* map.png - This map was generated using [mapchart](https://www.mapchart.net/usa.html). It shows the 10 states of interest for this project. These 10 states had the biggest differences between statewide gubernatorial and senate results.
* weighted_means_scatter.png - This scatter plot compares weighted means with actual election results. It shows a fairly linear relationship between the two. It also shows the weighted means are almost always lower than the actual result.
* sentiment_scatter.png - This scatter plot shows the spread of average sentiments and election results. It's useful for pointing out an outlier.
* top5.png - This bar chart displays the top 5 candidates with the highest average sentiment scores.
* bottom5.png - This bar chart displayes the bottom 5 candidates with the lowest average sentiment scores.

## Model
First, polls are given a weighted average with the weights being set by 538's grade of the poll. A simple linear regression model with just the weighted average as input is used as a baseline. Then the model is created using linear regression on the weighted averages and average social media sentiment. The final model is the same as the previous, but with one outlier removed.
## Conclusion
The project successfully shows that sentiment analysis of social media data can be a useful tool for forecasting elections. The model with average sentiment scores performed noticeably better on testing data than the baseline model only using weighted means of polling. Keeping in mind that the simplicity of this model made it easier to improve than its more sophisticated counterparts, social media data can be used to better predict election outcomes.