Handwritten Text Recognition (HTR) system implemented using TensorFlow 2.x and trained on the Bentham/IAM/Rimes/Saint Gall/Washington offline HTR datasets. This Neural Network model recognizes the text contained in the images of segmented texts lines.

Data partitioning (train, validation, test) was performed following the methodology of each dataset. The project implemented the HTRModel abstraction model (inspired by CTCModel) as a way to facilitate the development of HTR systems.

Notes:

All references are commented in the code.
This project doesn't offer post-processing, such as Statistical Language Model.
Check out the presentation in the doc folder.

Requirements
Python 3.x
OpenCV 4.x
editdistance
TensorFlow 2.x
Command line arguments
--source: dataset/model name (bentham, iam, rimes, saintgall, washington)
--arch: network to be used (puigcerver, bluche, flor)
--transform: transform dataset to the HDF5 file
--cv2: visualize sample from transformed dataset
--kaldi_assets: save all assets for use with kaldi
--image: predict a single image with the source parameter
--train: train model using the source argument
--test: evaluate and predict model using the source argument
--norm_accentuation: discard accentuation marks in the evaluation
--norm_punctuation: discard punctuation marks in the evaluation
--epochs: number of epochs
--batch_size: number of the size of each batch
