# NCSU-Short-Term-Solar-Forecasting

## Project Scope

- The main aim of this project is to explore state-of-the-art deep learning models to correlate continuous photovoltaic (PV) generation with contemporaneous images of sky captured using a fish-eye camera.
- Initially, we achieved excellent results on solar nowcasting task using our approach of applying state-of-the-art Vision Transformer (ViT) and comparing it with a  Convolutional Neural Network (CNN) baseline model.
- We extended the scope of our project to perform short-term (15-minute ahead) solar forecasting by experimenting with different image data stacking techniques to retain the temporal history and modified our ViT as well the CNN benchmark model to perform comparative performance analysis.

## Data acquisition 

The dataset used for this project has been acquired from Dr. Adam Brandt’s Environmental Assessment and Optimization (EAO) Group at Stanford University.

The specially collected dataset is called SKIPP’d – a SKy Images and Photovoltaic Power Generation Dataset which is complied to facilitate image-based solar forecasting and accelerate development of state-of-the-art deep learning models. 

The dataset acquired consists of 3 years of sky images (64 x 64) and concurrent photovoltaic (PV) generation data with 1-minute resolution. It contains few anomalies and missing data occurring from infrequent device reset / errors, data collection software errors, and camera replacement in middle of data collection cycle.

Sunny Days
![sunnygif_1](/images/sunny_day_demo_1.gif)
![sunnygif_2](/images/sunny_day_demo_3.gif)

## Nowcast Baseline model architecture 


## Nowcast Proposed Vision Transformer architecture 


## Nowcast Results


## Forecast Baseline model architecture 


## Forecast Proposed Vision Transformer architecture 


## Forecast Results
