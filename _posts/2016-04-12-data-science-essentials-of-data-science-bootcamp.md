---
layout: post
read_time: true
show_date: true
title: "Data Science: Essentials of Data Science Bootcamp"
date: 2016-04-12
img: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBRX1ni-6DxjzOMQMfIvckZ-3eu-DOm3Nq1nSAbzfmRrSDpD7_nt5bLAaQhaXLR17Xrgb0zfY30WXsmXJGGcjxza6CiaZMSAuIVF9fm2mSCDBg8KQun7Ld4pw05zv37Dr6VkdS4J7B8CI/s400/wordcloud_R.png
tags: [Data Science, Life in NYC, Text Mining]
category: Data Science
author: Strakul
description: ""
---

[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBRX1ni-6DxjzOMQMfIvckZ-3eu-DOm3Nq1nSAbzfmRrSDpD7_nt5bLAaQhaXLR17Xrgb0zfY30WXsmXJGGcjxza6CiaZMSAuIVF9fm2mSCDBg8KQun7Ld4pw05zv37Dr6VkdS4J7B8CI/s400/wordcloud_R.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBRX1ni-6DxjzOMQMfIvckZ-3eu-DOm3Nq1nSAbzfmRrSDpD7_nt5bLAaQhaXLR17Xrgb0zfY30WXsmXJGGcjxza6CiaZMSAuIVF9fm2mSCDBg8KQun7Ld4pw05zv37Dr6VkdS4J7B8CI/s1600/wordcloud_R.png)

  
About a month or so ago, I undertook a bootcamp called "[Essentials of Data Science](http://media.wix.com/ugd/3b731a_c09317e9b6b548d599c17607d14cf513.pdf)" and run by a handful of people with support from [NYCAscent](http://www.nycascent.org/). I've been meaning to write up a blog post about this, but only just now had the time. While I already had some knowledge of programming in R, I still learned a lot and feel far more confident about entering the data science job market now. Below, you'll find my general thoughts on the experience and a brief overview of what my project was about.  
  
**The Bootcamp**  
We met every Saturday for 5 weeks in a row from about 10am to 6pm. This was a bit of a grueling experience as even with frequent breaks, it's still a long period of time and it also took up half the weekend. I was pretty exhausted during these weeks, but enjoyed attending the meetings. We learned the basics of coding in R and how to utilize the variety of packages in R to do data science projects. There were also a few times when we discussed data science in general, job tips, and even a day where we had various guests to talk about data science with Python. Overall, I feel I know much better what it is to be a data scientist and what sort of skills I need to hone to be a successful one.  
  
I already knew a bit about R, having taken some Coursera courses on it. As such, the first few week was relatively easy for me. I thought Regression would be easy, having done some basic things as part of my astronomy career, but I was so wrong. The approach to Regression is very different in Data Science compared to my prior experience with Astronomy. For example, one typically defines a training set to fit models and then use those models on a test set to check how well the models perform. In my prior work, I treated everything the same; that is, I had no split between training and test data sets. In principle, this could lead to over-fitting the data so it was good to learn this. I certainly feel it's a more rigorous approach, provided that one has enough data to work with.  
  
I really liked learning about classification schemes for data. Regression trees are visually cool and random forests sound very powerful. Not sure how often that could be used in astronomy, given that so many quantities are numeric in nature, but it could perhaps be used when, say, you attempt to distinguish young stars from old stars. While we didn't explicitly cover Support Vector Machines (SVM), I read up on them and hope to apply that at some point as it sounds interesting and powerful.  
  
I was particularly interested in text mining and was happy we covered it in one of the latter sessions. While I had tried my hand at this [before](http://strakul.blogspot.com/2015/08/data-science-my-blog-with-r.html), I had not understood what I was doing as well as I do know. My project was a bit of a text mining exercise with Twitter data and I hope to continue exploring aspects of text mining in the future.  
  
We had a great team of people, both teaching the material and participating in the bootcamp. This was reflected in the final presentations, all of which I found to be very impressive. Topics included predictive models for Citibike usage, rat inspections, League of Legends win rates, terrorist suicide attacks, shoe prices, and Titanic survival rates. A broad range of interesting topics indeed!  
  
**My Project: Twitter Analysis with R and Shiny**  
For my project, I created an application with R's framework, [Shiny](http://shiny.rstudio.com/), and carried out a text mining exercise with Twitter data. Shiny apps are very easy to create, but I feel that comes at a sacrifice of control over what we can do. I'm sure you can style them to look however you want, but it takes a bit of work. What you gain, however, is the ability to quickly create dynamic, interactive plots and tables.  
  
My application, whose [source code is on Github](https://github.com/dr-rodriguez/Twitter-Analysis-Shiny-App), allows the user to gather Twitter English-language search data for any term they enter. I've since updated it to allow the user to query by user in addition to search terms. The most frequent 100 words are displayed as a word cloud for inspection purposes. The tabs on the top allow the user to navigate to the other options available in the application, which involve a bit of analysis.  
  
[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh6RmGoSLoB9CLtwbCxbDHffEughyd3HMkYuI-FJbFqap33mCIJrLf-9fTR1ODfxPZ_1udZ1hY8nFqIIhzUEADtScju1Hn-Uk0LQSV-xS9JxRPWUpvbFJ-Ly-qpteCWyJj8YafGtOCe0Ck/s400/Screen+Shot+2016-04-11+at+11.34.36+AM.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh6RmGoSLoB9CLtwbCxbDHffEughyd3HMkYuI-FJbFqap33mCIJrLf-9fTR1ODfxPZ_1udZ1hY8nFqIIhzUEADtScju1Hn-Uk0LQSV-xS9JxRPWUpvbFJ-Ly-qpteCWyJj8YafGtOCe0Ck/s1600/Screen+Shot+2016-04-11+at+11.34.36+AM.png)  
---  
Word cloud of Twitter search data (Data Science, 2000 tweets gathered on April 11, 2016).   
Stemming is used to group words together.  
  
There are two main things the application does. First, it does a sentiment analysis by comparing the words of each tweet to the [NRC Word-Emotion Association Lexicon](http://saifmohammad.com/WebPages/NRC-Emotion-Lexicon.htm), which has a list of words associated to 8 emotions (anger, surprise, joy, etc) and 2 sentiments (positive/negative). This is represented as a bar chart to demonstrate how the search query looks like when considering these emotions.  
  


[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhfwMKs1LIV_7q13e4K8jhiP6_JdNFow676_oFap4RrEZP1a81MoKduxFu-snD0IJ-fiAOwfFo2icyi0O0L1mLNyXDa6CdyE1_mgHx5nn-FRxPd7MvxGMhwsyQyDPTwv_pWhqUGP4WGV1E/s400/Screen+Shot+2016-04-11+at+11.34.45+AM.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhfwMKs1LIV_7q13e4K8jhiP6_JdNFow676_oFap4RrEZP1a81MoKduxFu-snD0IJ-fiAOwfFo2icyi0O0L1mLNyXDa6CdyE1_mgHx5nn-FRxPd7MvxGMhwsyQyDPTwv_pWhqUGP4WGV1E/s1600/Screen+Shot+2016-04-11+at+11.34.45+AM.png)

  
The second thing my application does is a Principal Component Analysis (PCA) on the word frequency of the 100 most common terms, eliminating the search terms. This is done since I wanted something numerical to plot and word frequencies for 140-character tweets are not that fun to look at. What the PCA does is construct new variables (aka, principal components) that are linear combinations of the word frequencies, with loading factors controlling how prevalent particular terms are for each new principal component. The factors are selected such that the variance is maximized in the subsequent principal components. In essence, and for this example, this is now exploring the prevalence of word combinations, or phrases, rather than individual terms. Tweets with high or low values of a particular principal component tend to be about the same topic.  
  
The subsequent tabs in my application allow you to explore the distribution of tweets in Sentiment-PC space as plots, tables, and a timeline (recently added). With these tools you can examine if there are interesting trends to the search term you are looking at. The newer version of this application uses Bokeh plots which allow the user to hover over the points to see the exact tweet being represented as well as pan and zoom in to regions of interest.  
  


[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgfdLmssOG4oO2O5IABiMSSz-caRSvfAoHO5IW0E6RG_e24ZDFm1NN_POKNUM46L7KY6t_FiuAjWzMTJvwvJSzLkuJJyy5oG9mF8AseahYVbuCdKjHS-qg4hcIhyoc8yx6hDuBwezkBKWQ/s400/Screen+Shot+2016-04-11+at+11.33.35+AM.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgfdLmssOG4oO2O5IABiMSSz-caRSvfAoHO5IW0E6RG_e24ZDFm1NN_POKNUM46L7KY6t_FiuAjWzMTJvwvJSzLkuJJyy5oG9mF8AseahYVbuCdKjHS-qg4hcIhyoc8yx6hDuBwezkBKWQ/s1600/Screen+Shot+2016-04-11+at+11.33.35+AM.png)

  
  
For my actual presentation, I went a few steps further. I gathered a bunch of tweets for a particular term, and then ran a variety of models comparing user information (eg, number of followers, number of favorites, etc) to attempt to predict where a user would fall on the PC spectrum. I looked at tweets about Microsoft and found that the second principal component was correlated to excitement about the Hololens for positive PC values and Xbox for negative PC values. In the end, my model performed a bit poorly, but it readily identified that the Xbox tweets were generally spam and had a rough set of metrics to select the type of people that would tweet about the Hololens vs general Microsoft tweets.  
  
I hope to improve the app a little bit to add some more descriptive text as to what it does. In the meantime, however, you can find a working version of it on [Shinyapps](https://dr-rodriguez.shinyapps.io/twitter_analysis/). This service hosts my application for a limited number of hours each month, so if you intend to use it heavily, I recommend grabbing the [source code](https://github.com/dr-rodriguez/Twitter-Analysis-Shiny-App) and running it on your machine and editing it to your needs.  
  
[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj4_Z25bvYOaRie03E5TtkP4lTb5e2VCCGN0JfOLa9ezcWWxfWWp05az6khpL_zcAFFZNo8Wj-G4mw1fW7RSRudQHJQGJWjxGnmdugOtdZJOVV7V4LNkrONPTNnFQ7rNuTbn70nd1fCps4/s400/rt_plot-1.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj4_Z25bvYOaRie03E5TtkP4lTb5e2VCCGN0JfOLa9ezcWWxfWWp05az6khpL_zcAFFZNo8Wj-G4mw1fW7RSRudQHJQGJWjxGnmdugOtdZJOVV7V4LNkrONPTNnFQ7rNuTbn70nd1fCps4/s1600/rt_plot-1.png)  
---  
Regression Tree analysis on Twitter search data (Microsoft). 
