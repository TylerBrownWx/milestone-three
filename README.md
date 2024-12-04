# Model Accuracy

Through Herbie functions we have the ability to import data from various models and different runs. With those runs, we are able to plot out different elements over various forecast hours, and ultimately help us see the accuracy of different models. In this code, we explored two models

* ECMWF: The European model, first used in 1979
* AI ECMWF: The European AI model, first used in 2023

Our overall goal of this project was to first understand how accurate the ECMWF was over a period of time, and then compare that to the AIFS to see if this model was more, or less accurate than the ECMWF.


## Exploring ECMWF Data

The bulk of the first half of the code is spent exploring the accuracy of the ECMWF through looking at data from a specific variable, geostrophic heights. In order to compare the accuracy of this model, two runs must be gathered:

* The forecast run, which will forecast for up to 240 hours
* The verification run, which will provide the run for the time that is being forecasted, therefore providing accurate data of what actually happened

Once both of these runs are obtained, various plots and maps are able to be created, all showing the error of the ECMWF runs at hour 0, hour 72, hour 144, and hour 240. And as one may assume, as you move farther into the future, the model becomes less accurate, which makes sense due to the unpredictability of our atmosphere. Finally, we are able to see the mean error over various forecast hours by combining all the data, which allows us to see were the ECMWF predicted above average heights, and where the ECMWF predicted below average heights.

## Absolute Error

The second half of our project uses a new variable, mean sea level pressure, which is easily able to be found through Herbie functions. Through near identical code used to find the difference before, we are able to find the absolute error over three different forecast ranges:

* Short Range: hours 12-60
* Medium Range: hours 72-144
* Long Range: hours 156-240

While it is fairly obvious that short range would have the least error and long range the most, through this one can see where this error is the greatest, and what locations the ECMWF is most accurate at.

## ECMWF vs. AI ECMWF
Finally, we want to compare the ECMWF and the AIFS, and this will be done by looking at the root mean square error. In this project, we first found the RMSE over 10 different ECMWF model runs to see the accuracy of the runs and how they changed over time. Like expected, the trend was that the error increased over time and by hour 240 most of the runs had a completely different RMSE. 

The final question was which model is more accurate, the Euro or the Euro AI. To investigate this we ran the same 10 model runs that were done above by instead in the AI ECMWF, and then plotted the RMSE against the ECMWF models. From this we found the AI ECMWF was more accurate, but it wasn’t by a lot and both were fairly similar.

## The Project
Overall, running through this code is a fun and informative way to see the accuracy of different models. We explored the ECMWF and AI ECMWF, but feel free to change some of the code and explore different models like the GFS or the HRRR.


## Installation
Running the code is fairly straightforward, just make sure you do a few things:

* Run all the import statements at the top of the code, without them many functions will not work.
* Run the Herbie functions near the top of the file. Feel free to change the date or the element that is being called, just make sure you put all the data into a variable.
* Enjoy the rest of the code. Feel free to change the forecast hours or other things you’d like, or even add new plots to show the error in other ways. The possibilities are endless!


## Contributions
Any contributions are welcome. If you have any ideas to improve the code, feel free to contribute!

## License
Add one


