# Real-Life-Projects

My case is on live data from Oil & Gas refinery.
The case is to predict Sulphur value on live Refinery data.
If sulphur content is high(above 7), refinery loose money. And Lab testing for sample is done max twice a day.
So can ML model use this live data from Exaqunatum & predict Sulphur. 
This is the business challenge.


It all numerical & a case of Regression. I tried most algos & tuned hyper param also.
Best result I was getting for LightGBM, then XGBOOST then catboost. 
Random Foreest also is OK. All gave ok result for train (0.65) but for test getting max of 0.47 as R2
Then used DEEP, used hyper params used Grid/random search,  Optuna, Byzentine. Got max of 0.74 for train but test again just 0.49.

Then used ML tools like Pycaret - got 0.36 as r2.
Out of all tools got best result from H2O - train r2 = 0.94 & test r2 = 0.54.
So yes overfiting is there.

The idea is to find cases early where Sulphur value is going beyond 7 or closing to 7.
So its absolute a must to find case when its approaching 7. The concern here is that when real life value is say 7.2, prediction comes as 5.
Now that dangerous as we will take wrong decision based on safe value of Sulphur of 5 where as its actually 7.2

Then tried SHAP, Shapash & explainerdashboard to find out which values are getting are affecting most when case of 7 is arising.
Found those. 

Now point is should we use weight on those columns or use SMOT or classification ..
All codes are uploaded here...
