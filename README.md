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
 








Finding price per square ft in the area


![image](https://user-images.githubusercontent.com/63114455/109431486-e4296580-7a2c-11eb-8901-347846b0f22f.png)












Finding relationships with RERA


![image](https://user-images.githubusercontent.com/63114455/109431516-120eaa00-7a2d-11eb-859c-15a9cfb91923.png)









Discrete




UNDER_CONSTRUCTION





![image](https://user-images.githubusercontent.com/63114455/109431550-34a0c300-7a2d-11eb-93c8-c16f76a70a31.png)












Inference- Data shows that majorly listed flats are under construction but Ready to move in flats have a slightly higher sale price value than under construction feature seems relevant but does not show very high relation







RERA






![image](https://user-images.githubusercontent.com/63114455/109431565-484c2980-7a2d-11eb-96a4-322f4def7763.png)













BHK_NO.







![image](https://user-images.githubusercontent.com/63114455/109431576-55691880-7a2d-11eb-9690-74e1f937c685.png)









READY_TO_MOVE






![image](https://user-images.githubusercontent.com/63114455/109431583-61ed7100-7a2d-11eb-9dbe-deef4038bad8.png)












Inference the feature seems to be a duplicate of Under construction status feature because shows in and either the same information more investigation is suggested






RESALE





![image](https://user-images.githubusercontent.com/63114455/109431611-7598d780-7a2d-11eb-8ead-d82100c0e690.png)















Inference- Features 'LONGITUDE' and 'LATITUDE' does not show any unique relevance as that part has already been covered by the city features hence these features should be excluded









Numerical
Continous






SQUARE_FT

![image](https://user-images.githubusercontent.com/63114455/109431644-93fed300-7a2d-11eb-8c72-f75ba5a30aa9.png)













![image](https://user-images.githubusercontent.com/63114455/109431647-99f4b400-7a2d-11eb-9250-60d3408cdbca.png)













![image](https://user-images.githubusercontent.com/63114455/109431656-a0832b80-7a2d-11eb-8e2a-e7a015385d69.png)















![image](https://user-images.githubusercontent.com/63114455/109431682-bd1f6380-7a2d-11eb-9ea2-16809ee49341.png)















Inference- The data shows that with increasing Square_fit area the price increases but after 18000 sqft the price starts to fall and the rapid difference is observed between 900 to 1500sqft beyond that its a gradual increase in the median price data shows a very high skewness due to outliers removal of the outliers is suggested
From the scatter plot we can observe that due to the outliers the feature does not show a clear line relation with the target variable removal of the outlier is suggested










TARGET(PRICE_IN_LACS)






![image](https://user-images.githubusercontent.com/63114455/109431712-ecce6b80-7a2d-11eb-9538-a0c5fc882e6e.png)





The variables are not normally distributed, including the target variable 'TARGET(PRICE_IN_LACS)'.
To maximise performance of linear models, we need to account for non-Gaussian distributions.







Transformation 


![image](https://user-images.githubusercontent.com/63114455/109431745-0f608480-7a2e-11eb-9e62-252a1e062368.png)










![image](https://user-images.githubusercontent.com/63114455/109431751-17b8bf80-7a2e-11eb-8383-e0632cb908f9.png)











Inference- from here we can observe that after the first log transformation the skewness has been considerably reduced but still the data skow high skewness and has outliers in it due to that linear relationship with the transformed target variable is still no a clear relationship 
Performing the transformation once again to see if makes any difference











Cardenal features 





![image](https://user-images.githubusercontent.com/63114455/109431777-361ebb00-7a2e-11eb-835c-a7ec6a62d2e4.png)













Final inference so selected features after EDA will be {'POSTED_BY', 'UNDER_CONSTRUCTION', 'RERA', 'BHK_NO.', 'BHK_OR_RK', 'SQUARE_FT', 'READY_TO_MOVE', 'RESALE', 'ADDRESS', 'TARGET(PRICE_IN_LACS)', 'City'} for further selection feature engineering and selection is needed 











The as the data was linear the model applied are 
1) linear regression as base 
2) Gradient boosting regressor
3) Random Forrest regressor 
4) XGB Regressor 

The best Result was obtained by XGB 






![image](https://user-images.githubusercontent.com/63114455/109431906-cceb7780-7a2e-11eb-85b5-f5af2767e3a9.png)
