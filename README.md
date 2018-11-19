# Dog-Breed-Identification

<b>Dog Breed Identification - Playground Prediction Competition on Kaggle</b>

The dataset was taken from Kaggle : https://www.kaggle.com/c/dog-breed-identification/data

Problem Statement : Identify 120 different breeds of dogs.

<b><h3>Approach :</h3></b>

<br>The train folder is divided into training and validation dataset.
<br>The split between training dataset and validation dataset is 80:20.
<br>All the image files are sorted into their respective breed's folder located in train and valid folder.

Data augmentation is applied to training set.
Operations performed :
<ul>
<li>Rescaling</li>
<li>Shearing</li>
<li>Zooming</li>
<li>Rotating</li>
</ul>
  
Image Data Generators are used to achieve data augmentation.

Transfer learning was applied as dataset was of small size :
<ul>
<li>Pretrained model InceptionV3 is used as base model.</li>
<li>Output of base model is fed to neural network with one layer of 256 units.</li>
<li>Dropout of 0.5 is taken. Reason for selecting high dropout rate is small dataset. Higher dropout trains the classifier more aggressively.</li>
<li>RMSprop was used as the optimizer while compiling.</li>
</ul>
  
<b><h3>For 20 epochs, results are :</h3></b>
<ul>
<li><b>95.10%</b> accuracy on training set.
<li><b>89.10%</b> accuracy on validation set.
</ul>

<h3>On submitting prediction of test set, loss of <b>0.39244</b> was achieved.</h3>
