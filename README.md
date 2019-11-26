# DrivenData-OpenAI-Caribbean-Challenge

Driven Data Competition - AI Caribbean Challenge: Mapping Disaster Risk from Aerial Imagery


[Follow the link]: https://www.drivendata.org/competitions/58/disaster-response-roof-type/page/142/



![alt text](https://github.com/i-mein/DrivenData-OpenAI-Caribbean-Competition/blob/master/images/drivendata.png)


In this challenge, your goal is to use provided aerial imagery (GeoTiff) to classify the roof material of identified buildings in St. Lucia, Guatemala, and Colombia. 


### Data 

- Metadata: CSV with metadata linking images (GeoTiffs) with corresponding train/test label files (GeoJSONs)


- Train Labels: The training labels in CSV format where each row contains a unique building ID followed by roof material (one hot encoded columns)


- Submission Format: The submission format


- STAC: A SpatioTemporal Asset Catalog of the imagery and labels



### ML Workflow

1. Download GeoTIFF + GeoJSON from STAC 

2. Summarize train data info (tiff_path, geo_path per roof_id etc)

3. Clip image tiles from Geotiffs based on GeoJSON data (transform ccoords system whenever it is required) x 7 regions

4. Reshape images with various sizes to (IMG_SIZE, IMG_SIZE, 3) for training   --> needs extra care !!

5. Form X, Y, i.e. features (pixels) and labels 

6. Save X, Y, to pickle for future use.. 

7. Feature Engineering - image transformations (optional)

8. Build DL model 

9. Train and evaluate model 

10. visualize and assess predictions 


### Repo still under development! (Final code will be publised after the competition end)


















