# reconstructing-obfuscations

A machine learning approach to beating facial image obfuscation (pixelation, blur, block) using Autoencoders. Explanations for our wok can be found in `Report.pdf`. This was our mid-semester project for Advanced Machine Learning (CS-408) at Ashoka University (in Spring 2019).

Trained models are available in the `trained_models/` directory. You can use them in conjunction with the `demos/` to see our models in action. If required, read below to replicate the training process. Folder names are self-explanatory.

Authors: [Prakhar Jain](https://github.com/prakhar171), [Harsh Karamchandani](https://github.com/harshk0525), [Dhruv Agarwal](https://github.com/agdhruv)

## Dataset
We use the Labelled Faces in the Wild (LFW) dataset from [here](http://vis-www.cs.umass.edu/lfw/#download). Download the dataset and place it in the root folder of the project in a folder named `lfw/`.

## How to Run

Note: This specifies the order of execution to replicate the project. File specific instructions are in the notebooks themselves.

Training Process:
1. Download the dataset and place it in `generate_datasets/` in a folder named `lfw/`. Currently, there is a partial LFW dataset present there.
2. Generate training datasets in pickle form.
	- Run `generate_datasets/dataset.ipynb` after making necessary modifications.
	- This will generate pickle files containing training images in `training_datasets/` in the root of the project.
3. Train (and test) the model(s).
	- Run `train.ipynb` in the root of the project after making necessary modifications.
	- You will need to install Tensorflow, Scikit-learn, Matplotlib, etc. to run this notebook.

Demo Process (demoing trained models):
1. First generate pickle files containing the files you want demo the models on. These files must be placed inside `generate_datasets/demo_images/`. You will see a few sample images (these are pictures of the authors).
	- Run `generate_datasets/dataset-for-demo.ipynb` after making necessary changes.
	- This will generate pickle files containing demo images in `demo_datasets/` in the root of the project. You will see sample pickle files in this folder, *which you can use to demo the project without going through the training process*.
2. Run the demos inside `demos/` in the project root.
	- Run the three demo files after making necessary modifications.