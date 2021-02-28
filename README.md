# House-price-prediction-
This dataset was done in team of two 
1) Ashish Sarkar 
2) Nikhil Rampuria 
The data was collected from kaggle.com 
Data had total 11 features including the target variable 

![image](https://user-images.githubusercontent.com/63114455/109431015-4896f580-7a2a-11eb-8df3-1ac3fbde9b15.png)



















The shape of the data was 
(29451, 12)




With no null values in the dataset 



EDA:- 
1)The address column had a very high cardenality 
  Top 15 address 
  ![image](https://user-images.githubusercontent.com/63114455/109431038-7da34800-7a2a-11eb-8655-a0c703290212.png)
  
  
  
  
  We observed that with specific address the data did not show much vriation with the target variable hence we converted the column to just city names and created a new variable     'city' and discarded the variable address 
2) POSTED_BY
   ![image](https://user-images.githubusercontent.com/63114455/109431125-d5da4a00-7a2a-11eb-8639-6b4054e315cd.png)
Inference- variable shows that Maximum listings were made by the dealers>Builders>Owners and Median prices goes in the range Dealer>Owner>Builder feature shows relation with the target variable and shows predictive nature
3)  BHK_OR_RK
    ![image](https://user-images.githubusercontent.com/63114455/109431140-eab6dd80-7a2a-11eb-98d5-0233ff054c1d.png)
Inference- Maximum flats listed are BHKs i.e 99.9% Rks are listed of 0.1%, BHK has higher median sale price value than RKs
4) City
Listing Count city wise
![image](https://user-images.githubusercontent.com/63114455/109431197-4b461a80-7a2b-11eb-9a3c-b34ff8ea2778.png)
   
   
   Median Sale Price     
   ![image](https://user-images.githubusercontent.com/63114455/109431235-716bba80-7a2b-11eb-9ce4-d034049ab156.png)
 
