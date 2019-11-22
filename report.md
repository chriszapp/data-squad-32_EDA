<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# EDA Report | Mental Health in the Tech Workplace in 2014

Maria João Silva<br>
22 November 2019


## Introduction

The goal of this project was to perform exploratory data analysis on a given dataset. This dataset, titled [Mental Health in Tech](https://www.kaggle.com/osmi/mental-health-in-tech-survey), originated from Kaggle and it contained the results of a voluntary survey conducted by OSMI, Open Sourcing Mental Illness, LTD, on tech industry workers in 2014. OSMI is a non-profit corporation based in Indiana, USA, dedicated to promoting mental health awareness and education in tech and open source communities. To this effect, they conduct annual surveys such as the one under analysis in this report.

The survey includes inquiries about multiple vectors of the work life of a tech industry worker, be they employees or employers, self-employed or remote workers. Participants are not geographically limited, nor is the survey exclusively directed at those afflicted with some form of mental illness. Without access to the questions of the 2014 survey, it is impossible to make judgements about bias in the responses. Given that the respondents were exclusively voluntaries, it might be argued that there is a form of selection bias: it is much more likely that only those tech workers who were already sensitive to health issues and/or aware of the OSMI corporation participated in the survey, rather than a sample that truly represented the whole population of tech industry workers.


## Goals

Given this possible bias, the questions that this report attempts to provide answers to mostly concern the slice of the population that identifies as suffering from some form of mental illness.

The main concern of this study was the characterisation of differences in approach and perception of mental health issues according to gender. To this effect, three different aspects were analysed:

1. In case of illness, what proportion of each gender has sought treatment?
2. How willing is each gender to talk about mental health issues in the workplace?
3. What differences are there in the perception of mental and physical health, particularly in the belief of negative consequences following the discussion of these issues with an employer?


## Process

After reading the dataset documentation, I discovered that there was no parameter that identified respondants who do suffer from mental issues/disorders and those that do not. The first step was to try to find a combination of other parameters that could give an indication of this information. For this purpose, two columns were used: "treatment" ("Have you sought treatment for a mental health condition?") and "work_interfere" ("If you have a mental health condition, do you feel that it interferes with your work?"). A positive response in either parameter indicated the existence of an issur. Negative values, however, were harder to treat, because absence of treatment does not determine absence of illness and the same is true of absence of work interference. yes / maybe not.

Looked at values in all columns to normalise and make sure that everything made sense. Changed "Gender", "Age", "self_employed".


## Description of results

Description of results
