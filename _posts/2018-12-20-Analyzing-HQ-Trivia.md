---
layout: post
title: Analyzing the actual data behind HQ Trivia
---

The popular game show app HQ Trivia was a viral sensation in late 2017 and early 2018. During this time a friend and I started manually collecting HQ trivia data. Stats such as how many people answered each question and what answers they chose, the different question categories, etc. in a spreadsheet. This became a daunting task and eventually we enlisted the help of mechanical turk where we created a task to reference recorded hq trivia games that were found on youtube and record the datapoints. This started to become costly so I then started to look at ways to collec this data without having to pay for mechanical turk or spend lots of time writing things down manually. 

# Data Collection Methods: 

## Machine Learning and OCR:
The first idea I had was to leverage optical character recognition. I created a python script which would take a list of youtube vidoes that users uploaded of their gameplay and downloaded each one to create a series of individual frames for each of the videos. I then trained a classification model to select the images we were most interested in to parse the text from those images. I used an OCR package to extract the questions, answers, and counts of answers. This worked fairly well however it was very prone to errors in the text recognitation. 

## Undocumented API:
During the rise of HQ trivia people started to create applications which would attempt to find the answers to the questions in real time so they could cheat and win the game. I started reading through the code of some of these applications and found that they were able to hook into the api that sends the game information to the HQ trivia app. Knowing this would be the best possible solution to data collection I quickly modified a python application that was used for cheating and instead inserted every data point I could find into a database. I setup a server to run this script and capture the afternoon and evening games that were broadcasted. 

## Data: 



# Analysis 



![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

models and experiments 

## Experiment 1 - full model on pct.change2 
```{r}
mod1 <- lm(pct.change2 ~ ticker + sumNegV + sumPosV + sumCompoundV + sumConL + sumLitL +sumNegL + sumPosL + sumSupL + sumUncert + count, data = ModelData, na.action = na.exclude)
summary(mod1)

plot(mod1)

#test$pred <- predict(mod1,test)

#test$residuals <- test$pred - test$pct.change2

```
