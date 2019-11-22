<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# EDA Report | Mental Health in the Tech Workplace in 2014

Maria João Silva<br>
22 November 2019


## Introduction

The goal of this project was to perform exploratory data analysis on a given dataset. This dataset, titled [Mental Health in Tech](https://www.kaggle.com/osmi/mental-health-in-tech-survey), originated from Kaggle and it contained the results of a voluntary survey conducted by OSMI, Open Sourcing Mental Illness, LTD, on tech industry workers in 2014. OSMI is a non-profit corporation based in Indiana, USA, dedicated to promoting mental health awareness and education in tech and open source communities. To this effect, they conduct annual surveys such as the one under analysis in this report.

The survey includes inquiries about multiple vectors of the work life of a tech industry worker, be they employees or employers, self-employed or remote workers. Participants are not geographically limited, nor is the survey exclusively directed at those afflicted with some form of mental illness. Without access to the questions of the 2014 survey, it is impossible to make judgements about bias in the responses. Given that the respondents were exclusively voluntaries, it might be argued that there is a form of selection bias: it is much more likely that only those tech workers who were already sensitive to health issues and/or aware of the OSMI corporation participated in the survey, rather than a sample that truly represented the whole population of tech industry workers.


## Goals

Given this possible bias, the questions that this report attempts to provide answers to mostly concern the slice of the population that identifies as suffering from some form of mental illness.

The main concern of this study was the characterisation of differences in approach and perception of mental health issues according to gender. To this end, three different aspects were analysed:

1. In case of illness, what proportion of each gender has sought treatment?
2. How willing is each gender to talk about their mental health issues in the workplace?
3. What differences are there in the perception of mental and physical health, particularly, do they believe that there might be negative consequences following the discussion of these issues with an employer?


## Process

### Preparing the data

After reading the dataset documentation, I discovered that there was no parameter that identified respondants who do suffer from mental issues/disorders and those that do not. The first step was to try to find a combination of other parameters that could give an indication of this information. For this purpose, two columns were used: "treatment" ("Have you sought treatment for a mental health condition?") and "work_interfere" ("If you have a mental health condition, do you feel that it interferes with your work?"). A positive response in either parameter indicated the existence of an issur. Negative values, however, were harder to treat, because absence of treatment does not determine absence of illness and the same is true of absence of work interference. After this process, a new column with True/False values was created called "has_illness". The key to these values is: True = "has illness"; False = "maybe not".

This was the biggest step in cleaning the dataset. After this, I looked at the other columns to ensure that all values were sensible. In particular, the responses to "Gender" were standardised, unreasonable "Age" values were excluded, and some of the NaN values in "self_employed" and "work_interfere" were filled, according to the data provided by related columns.


### Analysis
### Characterisation of differences in approach and perception of mental health issues according to gender

The first observation made was that there were approximately four times as many men as women who responded the survey. In order to have comparable quantities between genders, relative frequencies were used instead of absolute ones. The third gender category, "others" (including transgender, non-binary and unknown genders) was too small to be useable for this type of analysis (only 16 in a sample size of 1259). These 16 rows were dropped from the set.

The second observation had to do with the country of origin of the respondents. Given that gender issues may be culturally-sensitive, the nationalities included in the dataset were analysed. Most respondents came from western countries, with similar, or at least comparable cultural matrixes, so no further action was taken in this regard.


#### Subquestion 1: In case of illness, what proportion of each gender has sought treatment?

The data shows that 68.9 % of women suffering from mental illness have sought some form of treatment, while only 45.4 % of the men have pursued the same course. This is a significant difference (almost 25 %) in the average behaviour between genders.

<img src="/images/sq1.png" width="200"/>

#### Subquestion 2: How willing is each gender to talk about their mental health issues in the workplace?

Three different situations were considered: speaking about it with a coworker, with a supervisor, and during a job interview. There were few differences in the results obtained for each gender. The percentages were very close in all three situations. There was a slight tendency in women to be less open to discussing these issues with a supervisor and during a job interview (approximately 10 %).

<img src="/images/sq2.png" width="200"/>

The most obvious explanation hypothesis for this fact is that, given how few women (relatively speaking) are working in tech and how gender discrimination in the workplace is a continued issue, women may be less inclined to reveal a potential negative factor that could affect their position in that workplace (see subquestion 3 below). This is only an hypothesis, however. Further study would be required to either confirm or reject it as a related factor.


#### Subquestion 3: What differences are there in the perception of mental and physical health, particularly, do they believe that there might be negative consequences following the discussion of these issues with an employer?

In terms of physical health issues, there were few differences between the men and women. In general, men tended slightly to more easily reject the existence of negative consequences (approximately 10 % more), whereas women seemed more willing to give positive or ambivalent responses as to whether these consequences might exist (approximately 5 %).

<img src="/images/sq3.png" width="200"/>

The numbers were very different in regards to mental health, which indicates that, yes, the two types of issues are perceived differently. The percentages between response options ("Yes", "No", "Maybe") were almost equally distributed. Interestingly, the same difference that existed in regards to physical health was observed here: men tending more easily to a negative response, while women slightly preferred a positive or ambivalent one.


## Conclusions

The study revealed clear differences in the approach to mental health between genders. In case of illness, women appeared more likely to seek treatment than men. On the other hand, women were slightly less likely to disclose the existence of these issues in the workplace than men, be it with coworkers, supervisors or during interviews. In the case of both genders, physical and mental health issues are approached differently. There seems to be more openness towards the discussion of physical health issues than of mental ones.

Further studies could be conducted to further evaluate the weight of these differences, particularly comparing between job positions or years of experience working in the field. There might also be interest in studying which factors influence the differences noted between genders in subquestions 2 and 3.
