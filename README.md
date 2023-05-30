# NCSU-Short-Term-Solar-Forecasting

## Project Scope

- The main aim of this project is to explore state-of-the-art deep learning models to correlate continuous photovoltaic (PV) generation with contemporaneous images of sky captured using a fish-eye camera.
- Initially, we achieved excellent results on solar nowcasting task using our approach of applying state-of-the-art Vision Transformer (ViT) and comparing it with a  Convolutional Neural Network (CNN) baseline model.
- We extended the scope of our project to perform short-term (15-minute ahead) solar forecasting by experimenting with different image data stacking techniques to retain the temporal history and modified our ViT as well the CNN benchmark model to perform comparative performance analysis.

## Data Acquisition 

The dataset used for this project has been acquired from Dr. Adam Brandt’s Environmental Assessment and Optimization (EAO) Group at Stanford University.

The specially collected dataset is called SKIPP’d – a SKy Images and Photovoltaic Power Generation Dataset which is complied to facilitate image-based solar forecasting and accelerate development of state-of-the-art deep learning models. 

The dataset acquired consists of 3 years of sky images (64 x 64) and concurrent photovoltaic (PV) generation data with 1-minute resolution. It contains few anomalies and missing data occurring from infrequent device reset / errors, data collection software errors, and camera replacement in middle of data collection cycle.

<p>
  <ins>Sunny Days</ins>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <ins>Cloudy Days</ins>
  <br><br>
  <img src="/images/sunny_day_demo_1.gif">
  &nbsp;&nbsp;
  <img src="/images/sunny_day_demo_3.gif">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="/images/cloudy_day_demo_1.gif">
  &nbsp;&nbsp;
  <img src="/images/cloudy_day_demo_3.gif">
</p>

## Nowcast 

### Baseline Model Architecture 
<img src="/images/nowcast_cnn.png " alt= “” width="500" height="250">
<p>
  <img src="/images/nowcast_summary.png" width="300" height="150"/> 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="/images/nowcast_data.png " width="300" height="150"/>
</p>

### Proposed Vision Transformer Architecture 
<img src="/images/nowcast_vit.png" alt= “” width="500" height="250">

### Results
<img src="/images/nowcast_result.png " width="600" height="350"/>

## Forecast 

### Baseline Model Architecture 
<img src="/images/forecast_cnn.png " alt= “” width="500" height="250">
<p>
  <img src="/images/forecast_summary.png" width="300" height="150"/> 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="/images/forecast_data.png " width="300" height="150"/>
</p>

### Proposed Vision Transformer Architecture 
<img src="/images/forecast_vit.png" alt= “” width="500" height="250">

### Results
<img src="/images/forecast_results.png " width="600" height="350"/>

## Code Base
- nowcast.ipynb: Jupyter Notebook used to create the Vision Transformer nowcast model to correlate PV output to contemporaneous images of the sky, including model training, validation and testing.
- forecast.ipynb: Jupyter Notebook used to create the Vision Transformer forecast model to predict 15-min ahead minutely-averaged PV output, including model training, validation and testing.

## Dataset Description
- 2017_2019_images_pv_processed.hdf5: A file-directory like structure consisting of two groups: "trainval" and "test", for storing model development set and test set, respectively, with each group containing two datasets: "images_log" and "pv_log", which stores the processed images and PV generation data from all three years (2017-2019) in Python NumPy array format.
- times_traival.npy: Python NumPy array of time stamps corresponding to development set in .hdf5 file.
- times_test.npy: Python NumPy array of time stamps corresponding to test set in .hdf5 file.

Benchmark data available <a href="https://purl.stanford.edu/dj417rh1007"> here </a>
