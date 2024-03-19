# What is it?
I scraped some comments from Vk and conducted a small sentiment analysis with python colab
# How it works?
I extensively used pymorphy2 and dostoevsky python libs in this project. I also had to involve pandas, matplotlib for visualization and my own half-assed
transliteration system. The latter is used to determine the sex of the user by applying a combination of transliteration and pymorphy2 word analysis. However, 
my solution does not work with alphabets apart from latin. I combined 'positive' and 'negative' values in one feature for the sake of simplicity. The resulting 
number is scaled to the range from -1 to 1 (where 1 is for positive and -1 for negative messages respectively)
# What are the results?
The toxicity in the particularly chosen Vk group is following a normal distribution. 84% of comments were left by the male users. There is no obvious correlation between the neutrality and 'skipness' 
of a message for the dostoevsky library ('skip' is the value showing how hard it was for the dostoevsky model to classify the sentiment). Despite being 15% of the total comments, comments left by 
female users tend to be more positive in the scraped data (roughly by 8 percent more positive). Also, there is no correlation between the amount of comments of a user and the mean value of their toxicity.
# To improve
- Introduce better transliteration
- Migrate visualization from matplotlib to plotly
- Introduce a scraper for getting comments from the chosen Vk group
- Befriend the scraper and analyzer
