---
layout: post
title: Model selection VS Goodness of Fit
categories: [Statistics, Categorical_Analysis]
---

They both use log likelihood. 

They both use comparison between models.

## Model selection

More complex has the larger log likelihood.

The most complex model is called "**Saturated Model**".



A saturated model is one which **has as many estimated parameters as data points**. By definition, this will lead to a perfect fit and has largest log likelihood.



However, more complex model does not mean better model. Because we do not want too many parameters, which can cause over fitting.



In model selection, we compare two models' **log likelihood** as well as their **number of parameters**.

**A better model has fewer parameters without too much drop in log likelihood.**



This leads to the definition of **Akaike Information Criteria (AIC) **.



## Akaike Information Criteria (AIC) 


$$
AIC= 2 \times (\text{the # of parameters - log likelihood})
$$


**It is obvious that smaller AIC indicates a better model.**



**In model selection, we usually do not compare a model with the saturated one. Because the saturated model has little use statistically.**



## Goodness of Fit

Goodness of fit is also based comparison of log likelihood. 

In the computation of goodness of fit, we compare the log likelihood between the model and the saturated one. This leads to the definition of **Deviance**.

- Denote log likelihood of **Model M** as $$ \boldsymbol l_M$$
- Denote log likelihood of **Saturated Model** as $$\boldsymbol l_S$$

Then

$$
\boldsymbol{Deviance}= 2 \times \boldsymbol {(l_S-l_M)}
$$

**Deviance means the distance between the current model and the saturated one.**

As we can see, smaller deviance means better fit.



## Test for Goodness of Fit

$$H_0:$$
- The model M has enough goodness of fit
- All parameters existing in saturated model but not in M are redundant



The test statistic is the deviance of Model M. And it has approximately $\chi^2$ distribution with degree of freedom equal to 


$$
\text{# of observations} - \text{# of parameters in M} 
$$


In most cases, $$H_0$$ is designed to be rejected. However, this time, we may want it to be accepted.



Small p-value means lack of fit
