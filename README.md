# Arthropod taxonomy 
The purpose of these notebooks is to classify images of arthropods into one of 7 broad categories (taxonomical orders). The classifier is implemented in Python applying transfer learning using the MobileNetV3Small pre-trained model and the Keras library (Chollet et al., 2015). The results are evaluated in terms of accuracy.

## Setup
Clone the repo

```
git clone git@github.com:aot29/arthropod_taxonomy.git
```

Download the [Arthropod Taxonomy Orders Object Detection Dataset](https://doi.org/10.34740/KAGGLE/DSV/1240192) from Kaggle (Geir Drange, 2020).
__Unpack__ the data downloaded from Kaggle to the `arthropod_taxonomy/data` dir (create it if it doesn't exist).

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
* Save the prepared images

### [Classify](01_transfer.ipynb)
* Load pre-trained model
* Fit the model
* Evaluate

## References

 Geir Drange (2020). Arthropod Taxonomy Orders Object Detection Dataset. Kaggle. https://doi.org/10.34740/KAGGLE/DSV/1240192

 Chollet, F. et al. (2015), Keras, https://keras.io.
 