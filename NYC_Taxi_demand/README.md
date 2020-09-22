# NYC-Taxi-Demand-Prediction
### Data Information
Ge the data from : http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml (2016 data) The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC)

### Information on taxis:
Yellow Taxi: Yellow Medallion Taxicabs
These are the famous NYC yellow taxis that provide transportation exclusively through street-hails. The number of taxicabs is limited by a finite number of medallions issued by the TLC. You access this mode of transportation by standing in the street and hailing an available taxi with your hand. The pickups are not pre-arranged.

For Hire Vehicles (FHVs) 
FHV transportation is accessed by a pre-arrangement with a dispatcher or limo company. These FHVs are not permitted to pick up passengers via street hails, as those rides are not considered pre-arranged.

Green Taxi: Street Hail Livery (SHL) 
The SHL program will allow livery vehicle owners to license and outfit their vehicles with green borough taxi branding, meters, credit card machines, and ultimately the right to accept street hails in addition to pre-arranged rides.

Credits: Quora

Footnote:
In the given notebook we are considering only the yellow taxis for the time period between Jan - Mar 2015 & Jan - Mar 2016

### Data Collection
We Have collected all yellow taxi trips data from jan-2015 to dec-2016(Will be using only 2015 data)

![alt text](https://github.com/Krrish3398/ML_pet_projects/blob/master/NYC_Taxi_demand/data.png)


### ML Problem Formulation
Time-series forecasting and Regression


- To find number of pickups, given location cordinates(latitude and longitude) and time, in the query reigion and surrounding regions.
To solve the above we would be using data collected in Jan - Mar 2015 to predict the pickups in Jan - Mar 2016.

### Performance metrics
Mean Absolute percentage error.

Mean Squared error.

Unlike Pandas, operations on dask.dataframes don't trigger immediate computation, 
instead they add key-value pairs to an underlying Dask graph. Note that in the diagram below, circles are operations and rectangles are results.
to see the visulaization you need to install graphviz

![alt text](https://github.com/Krrish3398/ML_pet_projects/blob/master/NYC_Taxi_demand/mydask.png)

# Visualising the clusters on a map
![alt text](https://github.com/Krrish3398/ML_pet_projects/blob/master/NYC_Taxi_demand/download.png)

### Time series and Fourier Transforms
![alt text](https://github.com/Krrish3398/ML_pet_projects/blob/master/NYC_Taxi_demand/ft.png)
![alt text](https://github.com/Krrish3398/ML_pet_projects/blob/master/NYC_Taxi_demand/ft2.png)



### Conclusions
1. The above case study is about Taxi demand prediction in NYC.
2. In this case study we have to predict the number of pickups that could happen in a particular region in NYC.
3. Here we use Mean Absolute percentage error and Mean Squared error as Performance metrics. 3.Mean Absolute percentage error is given more importance as we want %error.
4. Here univariate analysis is performed on Pickup Latitude and Pickup Longitude, Dropoff Latitude & Dropoff Longitude, Trip Durations, Speed, Trip Distance etc.. and removel outlier/illegitimate values which may be caused due to some error. 5.Clustering of regions and time binning is performed as a part of datapreparation..
5. Fourier Features are obtained and by considering top 5 amplitudes and frequencies and adding those values to data as a part of feature engineering.
6. Triple exponential feature is performed as a part of feature engineering.
7. Then we apply this dataset on Baseline Model - Exponential Averages Forecasting -Linear Regression -Random Forest Regression -XgBoost Regression and we obtain MAPE 

---               Model                             Train MAPE         Test MAPE 

---         Baseline Model                         |     14%     |    13%    |
      
---      EXP_AVG Forecasting                       |     13%     |    12%    |
   
---         Linear Regression                      |     10%     |    10%    |
   
---    Random Forest Regression                    |      7%     |    9.7%   |
 
---         XgBoost Regression                     |     9.4%    |    9.3%   |
