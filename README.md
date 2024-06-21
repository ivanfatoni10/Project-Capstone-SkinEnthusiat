# SkinEnthusiast Model 

The project is based from Google Colab (due to limited system requirements of our laptop/PC). Using Machine Learning with Tensorflow as framework to Classify the skin disease. 

Link to Notebook: <br>
https://colab.research.google.com/drive/18sIG3Dl5Gmcz0Tlm5HOmHirAFc08qTth#scrollTo=H54bWB9HGFT2

## 1. Load Datasets 
  - Load Datasets from Modified dataset that we host to Google Drive, here is the link: <br> https://drive.google.com/drive/folders/1ZADZedxhYWruJxk2SFfd2etHEruzYDav

## 2. Pre-processing Datasets
  - Spliting datasets into:
    - 74% of train data
    - 19% of validation data
    - 7% of test data
  - Resizing the datasets into 150x150 and convert it to numpy array

## 3. Training
   - Using `Adam(learning_rate=1e-5)` as optimizer 
   - Added more layer too to `model.Sequential` to make model accuracy more better:
     -  Added `MaxPooling2D` layer
     -  Added `Flatten` layer
     -  Added `Dense(512, activation='relu')` layer 
     -  Added `Dropout(units=0.05)` layer
     -  Added more `Dense(units=13, activation='softmax')` layer
  - Training with 20 epochs 
  - From the result, got:
    - `loss: 0.38`
    - `accuracy: 0.83`

## 4. Saved the Model to Google Drive
  - Then, saved the model (*tf js format) to Google Drive (saved only the best model to Google Drive):<br>
https://drive.google.com/drive/folders/1b-oI_0IShqYNg0dYk6-Y4psmX6_gmHCg
