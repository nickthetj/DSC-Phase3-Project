# **The Road to Vision Zero**

## **Authors**:
Bobby Daly, DS; Michael Romanski, DS; Nicholas Tjandra, DS

![image](https://github.com/nickthetj/DSC-Phase3-Project/assets/126971652/9e88f1d6-2353-4ad1-95ec-1f7329edad13)



## **Overview**
The City of Chicago would like to gain more insight into traffic accidents given information about the car, the people in the car, and the road conditions. They plan on pursuing the goals of Vision Zero, an organization with a strategy to eliminate all traffic fatalities and severe injuries, while increasing safe, healthy, equitable mobility for all. Our project involves the examination of crash data sourced from the City of Chicago's Data Portal to further this mission. By analyzing this data, we hope to create a predictive model that can help evaluate trends across crashes. Through this comprehensive analysis, we will be able to make recommendations for Chicago to make their streets safer. 


## **Business Problem**
Vision Zero believes that the loss of even a single life is unacceptable. This is especially true because traffic accidents are not actually accidents at all; they are crashes, because they are preventable. In order to move Chicago closer to this vision, our data analysis led to the following recommendations:

Pedestrian/Cyclist Safety<br>
Traffic Rule Adherence<br>

Continue below to see how we arrived at these recommendations and what Chicago can do to prioritize these measures.

## **Data Understanding**
![image](https://github.com/nickthetj/DSC-Phase3-Project/assets/126971652/5bb378f0-e0b8-467f-bb04-e8fbb7767fa5)

The datasets used in this analysis come from the City of Chicago's Data Portal. We analyzed over 740,00 crashes from the City of Chicago's Data Portal ranging from 2016 to 2022. This data contained information on the [crashes]([url](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if)) themselves, the outcome of the [people]([url](https://data.cityofchicago.org/Transportation/Traffic-Crashes-People/u6pd-qa9d)) involved, and information on the [vehicles]([url](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3)) involved.

## **Data Preparation and Analysis**
A core component of Vision Zero is that the loss of even a single life is unacceptable. To gain insight into how to prevent deaths, we classified the data into two categories: crashes that resulted in Fatalities, and crashes that did not result in Fatalities. 

We trained a Logistic Regression Model as well as a Decision Tree Model. As Fatal crashes only consisted of about 1% of our dataset, we used a Pipeline to supplement the class with SMOTE to allow our model to better learn this category. We one hot encoded all 14 categorical columns which allowed the model to learn to classify each crash as Fatal or Not Fatal based on 238 features such as the weather, the time of day, the type of crash, and more. 

We tuned our model with GridSearch to constantly improve our recall score. We chose to focus on recall score to minimize the likelihood of our model predicting a crash as Not Fatal, when it was in fact Fatal.

## Recommendations
Our best model was the Logistic Regression with a recall score of .71. Inspecting the Coefficients, we found that HERE... were the most prevalent in predicting whether a crash would be Fatal or Not Fatal. 

To further investigate the crashes, we used the model to analyze which features were most prevalent in fatal crashes. 

**Budget**
For budget, our recommendation is that you have to spend money to make money. As we can see in our linear regression graph, our data suggests that the bigger the budget, the bigger the return. Furthermore the R^2 value suggests that the budget accounts for 63% of variance in worldwide gross. This, along with a p-value smaller than .05 from the anova, shows that we can reject the null hypothesis and say that a film's budget does impact it's worldwide gross.
![Screenshot 2023-08-04 at 3 35 16 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/93dea09e-ab2e-4161-94b5-f6649708e2a7)

**Genre**
For genre, we split movies out into each category they fell into and plotted the average worldwide gross by genre. Based on the graph below, we recommend creating adventurous, musical animations. These three genres had the highest average worldwide gross in our data and can easily pair well together in a film, as Olaf has proved.
![Screenshot 2023-08-04 at 3 36 28 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/ab293549-e729-4f8b-8cc4-950b9d146187)


**Director**
For director, we created a director rating by averaging all of the IMDb movie ratings for each director. From there we joined this data with the worldwide gross data to see which directors acquired the most gross across the globe. Directors have fans, and if you want to start building a brand, why not start with a director who has a large population already on board?

This graph represents the best available Directors who also are Writers for the films they make based on the director rating score we calculated. For Western-Centric audiences, we recommend Christopher Nolan, Damien Chazelle, or Wes Anderson. Nuri Bilge Ceylan did not have any data regarding budget and gross, so we do not feel comfortable selecting him. For the Indian Film market, S.S. Rajamouli would be an excellent selection as Director. Neeraj Pandey and Anurag Kashyap did not have any data regarding budget and gross, so we do not feel comfortable selecting them.

![Screenshot 2023-08-04 at 3 37 46 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/b0a0eae9-560f-46d1-81a0-e3e3ec4ba467)
![Screenshot 2023-08-04 at 3 37 21 PM](https://github.com/rbdaly16/Movie-Data-Analysis/assets/126971652/d49a1900-1d35-4433-a647-a6c014c154ad)


## **Next Steps**
There are a few steps we would like to take to further limit fatalities in car crashes:<br>
1. Crash Location Investigation
2. BAC Investigation
   
The datasets we worked with provided some information available on the location of every crash, but it was broken down by street. It might be easier and more efficient to break the city down into areas or districts to highlight particular problem areas of the city that could be reformed.

Furthermore, the top preliminary cause and fatal percentage of fatal crashes was the Physical Condition of the Driver. With more time we could investigate how much of this was due to drunk drivers or drivers under the influence of drugs.

## Thank You!
Thank you for taking the time to review our recommendations.
We hope this information helps and we look forward to working with you more on the next steps.

Sincerely, <br>
Bobby Daly, Michael Romanski, Nicholas Tjandra <br>
Airflix Studios

## Further Details
Further details are available in the full analysis presented in the CHANGE THIS! -> [Jupyter Notebook](https://github.com/rbdaly16/Movie-Data-Analysis/blob/bobby/Movie%20Data%20Analysis.ipynb). 

## Repository Structure
```
├── data
├── Scratch_notebook_folder
├── images
├── README.md
├── .gitignore
├── .DS_Store
├── Movie Data Analysis Presentation.pdf
└── Movie Data Analysis final.ipynb
```
