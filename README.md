# Comparison of sentiment analysis and stance detection for social media data

This project was conducted between René Steeman and Anna Fernandez-Rajal, as part of the course [II2202 Research Methodology and Scientific Writing](https://www.kth.se/student/kurser/kurs/II2202?l=en)

With social media being used in the spread of misinformation, it is important for users to be presented with a wide range of viewpoints instead of being limited to their filter bubble with misinformation. The recommended systems that are used to rank the posts that are visible to the user can lead to selective exposure, which leads to such systems not achieving one of the main functions of news, namely to "provide fair and full information so citizens can make sound political choices". One of the ways that this can be combated is by using diversity measures to improve the diversity of suggested results with sentiment being one possible metric.

However, sentiment analysis is limited to only indicating if a text is positive, neutral, or negative. If you would want to promote diversity of opinions, this might not be enough. The technique of stance detection, which is used to indicate if a text is in favor, neutral towards, or against a certain target (which could be a statement such as "pizza is amazing") might be more suitable. While sentiment and stance may seem similar, they can have very different meanings. One example would be "I think candidate Y is the best", which has a positive sentiment, but if the target would be "I hope candidate X wins", stance detection would rate it negatively. Therefore, there is no direct mapping between sentiment and stance, as it is dependent on the context. A major downside of employing stance detection to help diversify the results of a recommender system is the need for this target, which would be difficult to generate automatically from a short text and the creation of a large enough array by hand would be incredibly time-consuming. Even if stance detection would be able to provide better results, it might still not be worth using because of this issue.

In this project we will analyze how well each technique performs on short text, in the form of tweets, to see how accurate they are within their own domain. Then, an analysis follows for how similar their results are and how they relate. Finding out which technique might be most suitable for use in a diversified recommender system.


### Dataset
The data has been collected from the [SemEval 2016 task 6a dataset](https://aclanthology.org/S16-1003/). This contains nearly 5k tweets and
ground-truth values for both sentiment and stance. Of all the data, 4163 are for the training set and 1249 for
testing, belonging to five topics of a debate common at the time in the United States, ‘Atheism’, ‘Climate
Change is a Real Concern”, ‘Feminist Movement’, ‘Hillary Clinton’, and ‘Legalization of Abortion’. 
