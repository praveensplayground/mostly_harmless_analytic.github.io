---
layout: post
title: Econometric methods in impact evaluation
subtitle: How economists can be a better causality estimator
cover-img: /assets/img/high_impact.jpg
thumbnail-img: /assets/img/high_impact.jpg
share-img: /assets/img/path.jpg
tags: [books, test]
---

Economists are often mistaken as the ones who only advise politicians on how to implement policies. Of course, they are the ones who support implementing minimum wages or oppose trade tariffs. They are also seen working at central banks, trying to shape the monetary policy of a country or managing a mutual fund at a large investment bank. However, few people outside the discipline know that economics is a very practical science which largely deals with data. 

### What is econometrics
Econometrics is the branch in economics which contains a wealth of statistical and mathematical tools used in data analysis and data science. For economists, data represents the signals how the firms or individuals in an economy act in order to maximize their well-being subjected to a set of constraints. It is a very causal science, meaning that the economists will be preoccupied with understanding whether A causes B but not B causes A. which will consequently make them invest a lot of time ensuring the causality is effective, and not an accidental correlation. 
Economists are obsessed with developing a perfect counterfactual.  In order to measure the effect of a policy change or any other intervention, we need to observe the difference between a world that has implemented the policy and the counterfactual world where it has not. We only get to live in a one world which is the world where the policy has occurred. We do not have the luxury to create a similar world where the policy has not occurred in order to compare. A good economist is able to construct a near-perfect counterfactual in order to compare the two states. One technique used, often prove to be quite naive, is to compare the pre and post implementation. Consider measuring the impact of a tax cut on laptops. In this case, the change in demand over time could be due to the tariff or change in any other macro-economic variable that occurs over-time such as business cycle fluctuations. It could also be that the demand for laptops are going up anyway. Therefore the pre-post analysis fails to capture the underlying trends. Consider comparing the outcomes of the treatment group and the control group during the treated time period. Here there is no guarantee that socioeconomic characteristics are affecting the groups the same way. Maybe these features are not in the dataset or they are fundamentally unobserved. Controlling for all these characteristics are thus difficult. This is where Difference in Difference (DiD) method comes to rescue.

### Difference-in-Difference Estimation
DiD puts together the before-after and treatment-control group comparison. Its applications are widespread in economics, policy, business and various other fields. DiD employs a unique method that gives its name. This requires a panel dataset for a treatment and control group. In the DiD method we deduct the before-after difference of the control group and deduct that from the same in the treatment group. This method succeeds in achieving two goals. Firstly, any changes that are happening over time such as the effect of fluctuating economic cycles is nullified.  Secondly, any characteristics that determines the outcomes of the treatment and the control group are also accounted for so long as they are constant across time. Thus, the time variant and time invariant differences that are difficult to observe are accounted for.  


![Did_image](/assets/img/did_pic.jpg)



### Estimating the Model
A well defined regression model allows you to estimate the causal effect with any other control variables. We will use dummy variables to define the before and after states and treatment and control group differences. The full model will be a one with dummy variables with an interaction variable. We will skip the mathematical derivation and look at the result below.


![Did_equation](/assets/img/did_equation.PNG)


### Equal trends assumption
The researcher needs to convince the audience that “equal trends” assumption holds between the treatment and control groups over-time. Essentially, we need to ensure that the treatment group and the control group are affected equally by any trends that are occuring across time. If the trends look terribly different across time for the two groups, the estimates could be biased. There are no specific tests that can be run and often time-series graphs will do the job. This is the assumption that often hardest to fulfil in a DiD study. Therefore the success of the study hangs on your ability to find a control group that satisfies this assumption. Apart from the equal trends assumption, we have to make sure there are no spillover effects from the treatment manifesting in the control group. 

One very important factor to consider is that since we are using a panel dataset, the datapoints are serially correlated. Accounting for the serial correlation is paramount in order to maintain the homoscedasticity assumption in linear regression. The method is also a very flexible method which we can combine with other methods such as fixed effects method. DiD has produced great results especially when we do not have the luxury to conduct a comprehensive experimental design. This is one of the number of panel-data methods that are employed in the field of economics. This method could be especially handy in order to measure the impact in a time of pandemic where finding a baseline would be almost impossible through conventional methods. 

( _This article was originally published in Octave: John Keells Medium page._ )
-Praveen Ekanayake-
