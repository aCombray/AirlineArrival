# AirlineArrival
This is a project to predict whether a fight will arrive late. 
<br>
The data is from https://www.transtats.bts.gov/Fields.asp?Table_ID=236 .
<br>
Explain the data https://www.transtats.bts.gov/DatabaseInfo.asp?DB_ID=120&DB_URL= .
<br> 
The key is the engineered feature 'DEP_DELAY/CRS_ELAPSED_TIME'. Using Logistic regression on this feature, we achieve f1 score 0.92 and accuracy 0.92, which is quite good. 
## Conclusion
The conclusion is the engineered feature 'DEP_DELAY/CRS_ELAPSED_TIME' alone can predict the arrival delay very well. The explaination is that the makeup minutes / flight minute is almost fixed. The longer the flight is, the more delayed time can be saved. It basically determines whether a flight will arrive at the destination on time. All other features may be used to make further corrections if we use boosting methods.
<br>
This prediction is based on the condition that we have the information about the departure. That is the prediction can only be made after the flight takes off. However, if we want to predict delays before the departure, we need to predict the departure delays as well. For that case, it is better to include weather data. Moreover, if the target flight is scheduled late in the day, we can also include data about the early delays of filghts. 
