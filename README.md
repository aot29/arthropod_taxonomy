# Arthropod taxonomy 
The purpose of these notebooks is to classify images of arthropods into one of 7 broad categories (taxonomical orders). Three algorithms are compared: Support Vector Machine, Multilayer Perceptron and Random Forest. The classifiers are implemented in Python using the Scikit-Learn library (Pedregosa et al., 2011). For each classifier, optimal parameters are determined using grid search. The results are evaluated in terms of accuracy and execution speed.

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
* Reformat the images
* Create feature matrix


## References

 Geir Drange (2020). Arthropod Taxonomy Orders Object Detection Dataset. Kaggle. https://doi.org/10.34740/KAGGLE/DSV/1240192

 Pedregosa et al. (2011), Scikit-learn: Machine Learning in Python, JMLR 12, pp. 2825-2830.
 