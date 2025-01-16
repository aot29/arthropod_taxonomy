# Arthropod taxonomy 
The purpose of these notebooks is to classify images of arthropods into one of 7 broad categories (taxonomical orders). The classifier is implemented in Python applying transfer learning using the MobileNetV3Small pre-trained model and the Keras library (Chollet et al., 2015). The results are evaluated in terms of accuracy.

## Setup
Clone the repo

```
git clone git@github.com:aot29/arthropod_taxonomy.git
```

Download the [Arthropod Taxonomy Orders Object Detection Dataset](https://doi.org/10.34740/KAGGLE/DSV/1240192) from Kaggle (Geir Drange, 2020).
__Unpack__ the data downloaded from Kaggle to the `arthropod_taxonomy/data` dir (create it if it doesn't exist).

Create a 'models' directory, if it doesn't exist. Trained models will be stored here.

Setup a Python venv

```
python -m venv at_venv
source at_venv/bin/activate
cd arthropod_taxonomy/
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

### [Compute a baseline, classify using SVN](01_baseline_svn.ipynb)
* Load the images prepared in previous notebook
* Compute a baseline
* Classify using Support Vector Machine

### [Classify using CNN](02_cnn.ipynb)
* Load the images prepared in previous notebook
* Classify using Convolutional Neural Network

### [Classify using transfer learning](03_transfer.ipynb)
* Load the data
* Load pre-trained model MobileNetV3Small
* Fit the classifier including the pre-trained model and a dense network
* Save the fitted classifier

### [Evaluate](04_evaluate.ipynb)
* Load the previously trained models
* Load the test data
* Evaluate the accuracy and inference speed of each model

## References

 Geir Drange (2020). Arthropod Taxonomy Orders Object Detection Dataset. Kaggle. https://doi.org/10.34740/KAGGLE/DSV/1240192

 Chollet, F. et al. (2015), Keras, https://keras.io.
 