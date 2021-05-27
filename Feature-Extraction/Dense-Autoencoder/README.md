# Subdirectory for Feature Extraction with a Fully-Connected (Dense) Autoencoder

Autoencoders are a rather interesting type of model. Rather than the conventional supervised/unsupervised learning paradigms, autoencoders are self-supervised. They perform learning on the unlabeled dataset in order to learn transformations to that dataset for achieving particular goals. For the project in this subdirectory, we will be using a fully-connected (dense) neural network to act as the autoencoder. The autoencoder will learn to compress the original MNIST handwritten digits dataset from $28 \times 28$ datasets down to a $7 \times 7$ representation. 

We note that this isn't necessarily a simple resizing of the images using something akin to JPEG compression. Rather, the dense autoencoder will learn which features from the original images are most important for it to know in order to reconstruct the original dataset. The behavior is not necessarily as predictable as a simple resizing because the features which the model decides are most important may not always be the same. 

## FILE: Dense_Autoencoder_Feature_Extraction.ipynb

This file is a fully-documented Jupyter Notebook which contains the source code of the project. Feel free to read through the documentation of the notebook in order to see the output and gain a more thorough understanding of the operations within. GitHub supports viewing the Jupyter Notebooks. If it fails to load initially, click the reload button on the page. The documentation, the code cells, and all of the output cells shoulld properly load within your browser.

## FILE: dense-raw-classifier-model.h5

This file is a checkpoint created during the most recent runtime of the notebook. It contains the weights for the classifier demonstrated for use without performing encoding first. That is, the baseline example which classifies the digits of the unaltered images in order to gain a frame of reference for the performance impacts of the autoencoder approach. The file can be loaded in order to extract the exact same model used in the notebook shown. If you run the notebook on your own, the file will be overwritten during training. 

## FILE: dense-autoencoder.h5

This file is a checkpoint created during the most recent runtime of the notebook. It contains the weights for the autoencoder demonstrated for use when compressing the image down to $7 \times 7$ (one sixteenth the original number of pixels) and reconstructing the original images back to this size. The file can be loaded in order to extract the exact same model used in the notebook shown. If you run the notebook on your own, the file will be overwritten during training. 

## FILE: dense-encoded-classifier-model.h5

This file is a checkpoint created during the most recent runtime of the notebook. It contains the weights for the classifier demonstrated for use when performing encoding first. That is, the final example which classifies the digits of the encoded images in order to demonstrate the performance impacts of the autoencoder approach. The file can be loaded in order to extract the exact same model used in the notebook shown. If you run the notebook on your own, the file will be overwritten during training. 
