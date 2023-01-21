# River 

## River Stage level prediction using images

## Content
* [Problem](#problem)
* [Dataset](#dataset-predictions)
* [CNN](#cnn)
* [Images](#images)

### Problem
The objective of this project is to create an AI model to predict the level of Stage seeking to implement the same strategy for other values such as Discharge.

Currently these values are obtained from sensors in the river, we have values since 2012, the problem with the sensors is the cost of keeping them working correctly and the cost of buying them whenever necessary.

### Dataset predictions
With the provided dataset we were able to create some regression models using libraries such as statsmodels or sklearn, these models use characteristics such as the white water present in the images, Gray scale mean of all the pixel intensities, Mean of all the pixel intensities in the saturation channel or Maximum pixel distance from weir line to whitewater raw down.

We cleaned the data before being able to process it, we defined which variables were relevant to take them into account and which were not to be able to rule them out in our models, we treated the outliers to understand their meaning and see the impact they had on our results

### CNN
Seeking to avoid the use of sensors in the river to save costs of keeping the sensors working and repairing them in case of damage, another option is on the table, trying to predict the values using only images of the river.

To explore this option, we created CNN models that seek to analyze the information contained within the images, this information could be useful to predict the level of the scenario.

The size of each image could be a problem considering the number of images, for this reason we reduced the images to a size of 512 x 512 and then divided the set into three groups (training, test and validation), then divided the images into three groups we can use in the model we build. We tried to focus mainly on three features that we found useful in this case:
* #### The Full Picture 
    The full picture might contain necessary, scenario-level-correlated information that we probably can't see
* #### White water 
    The foam in the water is an indicator of the amount of water that runs on the water
* #### Borders
    The river borders establish the limits of the area used by the river and can tell us important information
### Images
Variety of images provided
<br>
<img src="Images/StateLineWeir_20150901_Farrell_009.JPG" width=330>
<img src="Images/StateLineWeir_20140427_Farrell_010.JPG" width=330>
<img src="Images/StateLineWeir_20140427_Farrell_015.JPG" width=330>
<img src="Images/StateLineWeir_20140430_Farrell_084.JPG" width=330>
<img src="Images/StateLineWeir_20141120_Farrell_289.JPG" width=330>
<img src="Images/StateLineWeir_20150103_Farrell_010.JPG" width=330>
