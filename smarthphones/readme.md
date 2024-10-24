OBJECTIVES
We were contacted to create a model capable of identifying when a mobile phone appeared on screen. We then set the following objectives (see extraerframes.ipynb):

To be able to obtain multiple images of mobile phones in various situations to generalize the model as effectively as possible.
Perform labeling in YOLO format, as we focused on transfer learning using an already functional neural network.
Execute the transfer learning process.
Present some videos demonstrating our results.
APPROACH AND DEVELOPMENT
I will briefly explain the development process.

Initial Setup and Process
First, I’ll outline the modus operandi and how things proceeded.

We planned the entire development process to be executed in YOLO format, since, in order to retrain this neural network, we needed to label everything in YOLO's specific format.

This step is crucial because we need to label each image individually to train the YOLO v3 neural network.

Once we had downloaded and labeled the images, the next step was to generate a .data file (creacion-data.ipynb) containing information on the locations of train.txt, test.txt, class.names, and the backup where the generated weights would be stored. The train.txt and test.txt files must contain the paths to each image, and each .jpg image must have a .txt file with the same name and location, following the YOLO format to specify where each class to classify is located.

Once all this was set up, we needed to proceed with transfer learning. Before performing the transfer learning process, we had to make a modification to the neural network architecture. Since it was originally trained on 80 classes, we adjusted the structure to fit our specific parameters.

With this done, we proceeded with the transfer learning process (transfer-learning.ipynb), which took about 6 hours.

Finally, we carried out a classification on new videos we obtained (movil-reentreno.ipynb).
