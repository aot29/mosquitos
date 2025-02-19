# Mosquitos 
The purpose of these notebooks is to classify images of mosquitos into one 
of 3 categories (species). 
The classifier is implemented in Python applying transfer learning using 
the MobileNetV3Small pre-trained model and the Keras 
library (Chollet et al., 2015). 
The results are evaluated in terms of accuracy.

## Setup
Clone the repo

```
git clone git@github.com:aot29/mosquitos.git
```

Download the [(Original Images) dataset of Vector Mosquito Images](https://data.mendeley.com/datasets/88s6fvgg2p/4) from Mendeley (Pise et al., 2022).
__Unpack__ the data downloaded from Mendeley to the `data` dir (create it if it doesn't exist).

Create a 'models' directory, if it doesn't exist. 
Trained models will be stored here.

Setup a Python venv

```
python -m venv at_venv
source at_venv/bin/activate
cd mosquitos/
pip install -r requirements.txt
```

Start the notebook

```
source ../at_venv/bin/activate
jupyter lab
```

## Notebooks

### [Process data](00_process_data.ipynb)
* Crop and reformat the images
* Split the data into train/validate/test datasets
* Save the prepared images

### [Classify using transfer learning](01_classify.ipynb)
* Load the data
* Compute a baseline
* Load pre-trained model MobileNetV3Small
* Fit the classifier including the pre-trained model and a dense network
* Save the fitted classifier
__Evaluate__
* Load the test data
* Evaluate the accuracy and inference speed of the model

## References

 Pise, Reshma; PATIL, Kailas; Laad, Meena; Pise, Neeraj (2022), “Dataset of Vector Mosquito Images  ”, Mendeley Data, V4, doi: 10.17632/88s6fvgg2p.4

 Chollet, F. et al. (2015), Keras, https://keras.io.
 
