# Modeling Mental Health
**Wendy Matta, Abhas Wanchu, Michael Garfagnoli, Aimee Williams, Nura Hossainzadeh**

## Summary
In this project, our team uses machine learning models to gauge the mental health of the authors of short statements that were posted in online forums. Ultimately, our two most performant models were a binary model with a weighted F1 score of 96% and a multiclass model with a weighted F1 score of 85%. 

**This repo is designed to run inside of google collab due to several dependencies on the `google.colab` library as well as the fact that the training, test, and validation data is saved to the end user's google drive.**

## Flow
1. `207_Final_Data_Preprocessing`
generates all of our training, validation, testing data into Google Drive.
2. `207_Final_Experimental_Models` is optional and contains models that improved over our baseline but were not chosen. 
3. `207_Final_Models` contains our most performant models, one binary and one multi-class. It should be noted that it also transforms the original dataset from the first notebook. For the binary model, it transforms the data into bag-of-words.

## Usage
This repo is intended for use with Google colab, and some libraries may not be available for immediate use.

1. Clone this repo into a Colab environment of your choice.
2. In a new notebook, run the following command: `!pip install -r requirements.txt`.
3. Execute the notebooks in the order mentioned in `Flow`. You will be prompted at the end of the first notebook to authorize Colab to access your Google drive to update the feature and response variable datasets as well as the beginning of `207_Final_Models.ipynb` for read access.
4. To save either model for usage in other projects or applications, a simple `model.save('/content/mydrive/models/model_name', save_format='h5')` command will save either the binary or the multiclass model as a file that can later be loaded using tensorflow with `model = tf.keras.models.load_model('content/mydrive/models/model_name')`These commands can be appended to the bottom of `207_Final_Models.ipynb` at your discretion.

