---
layout: post
title: You're up and running!
---

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

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
