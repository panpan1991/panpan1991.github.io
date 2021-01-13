---
layout: post
title:  Intuitive Understanding of General Regressions
categories: [Statistics, General_Regression]
---

In

$$ logit(\pi)=\beta_0+\beta_1 x $$

or 

$$ probit(\pi)=\beta_0+\beta_1 x $$


They are actually using the CDF of logistic distribution and normal distribution to fit the function

$$
\pi=f(x)
$$


Since $$f(x)$$ is sigmoid, it cannot be fitted using a strait line. Instead, it has to be fitted with CDF.

But some CDFs, such as the CDF of F distribution and $$\chi^2$$, cannot be used to fit $$f(x)$$.



## Separation theorem

- $$\beta_0$$ is the location parameter
- $$\beta_1$$ is the scaling parameter



If we want  to fit **complete separation**

- $$\hat{\pi}=0$$ for $$x\leq x_0$$ 
- $$\hat{\pi}=1$$ for $$x> x_0$$ 

or 

**quasi-complete separation**

- $$\hat{\pi}=0$$ for $$x< x_0$$ 
- $$\hat{\pi}=0/1$$ for $$x=x_0$$ 
- $$\hat{\pi}=1$$ for $$x> x_0$$ 

We increase the $$\beta_1$$ to $$\infty$$
