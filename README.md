# Forest_Cover
 Problem statement was to build a classification methodology to predict the type of forest cover based on the given training data. 
 
# Data Description
 Name / Data Type / Measurement / Description
 Elevation / quantitative /meters / Elevation in meters
 Aspect / quantitative / azimuth / Aspect in degrees azimuth
 Slope / quantitative / degrees / Slope in degrees
 Horizontal_Distance_To_Hydrology / quantitative / meters / Horz Dist to nearest surface water features
 Vertical_Distance_To_Hydrology / quantitative / meters / Vert Dist to nearest surface water features
 Horizontal_Distance_To_Roadways / quantitative / meters / Horz Dist to nearest roadway
 Horizontal_Distance_To_Fire_Points / quantitative / meters / Horz Dist to nearest wildfire ignition points
 Wilderness_Area (4 binary columns) / qualitative / 0 (absence) or 1 (presence) / Wilderness area designation
 Soil_Type (40 binary columns) / qualitative / 0 (absence) or 1 (presence) / Soil Type designation
 Cover_Type (7 types) / integer / 1 to 7 / Forest Cover Type designation.

# Data Validation
 We validate the name of the files based on the given name in the schema file. We have created a regex pattern as per the name given in the schema file to use for validation. After validating the pattern in the name, we check for the length of date in the file name as well as the length of time in the file name. If all the values are as per requirement, we move such files to "Good_Data_Folder" else we move such files to "Bad_Data_Folder."

# Model Training
  KMeans algorithm is used to create clusters in the preprocessed data. 
The optimum number of clusters is selected by plotting the elbow plot, and for the dynamic selection of the number of clusters, we are using "KneeLocator" function. The idea behind clustering is to implement different algorithms ,to train data in different clusters. The Kmeans model is trained over preprocessed data and the model is saved for further use in prediction. 

# Prediction
Based on the cluster number, the respective model is loaded and is used to predict the data for that cluster.













