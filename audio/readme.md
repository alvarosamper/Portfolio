OBJECTIVE:
For the later development of a mobile app, we were tasked with creating a dataset of sounds that could be disturbing to certain people.
Once the dataset was created, we needed to train a neural network capable of reading .wav files and classifying them.
SUMMARY:
To train this model, we conducted a transfer learning exercise based on the Yamnet neural network.

The most extensive part of the project was creating the dataset, which is crucial as the results heavily depend on its quality. We had to gather the data ourselves.

Specifically, the process involved searching for and downloading audio from videos that contained relevant sounds. We then used a web app to cut the .wav files, labeling them with the desired sound class. In total, we created a dataset with 317 .wav files across 10 different classes:
classes = [firecrackers, gunshot, drill, screams, dogs, car horns, alarms, blender, vacuum cleaner]

Once this was done, we transformed the .wav files into 16-bit tensors with a dimension of 1024, as this is how the network was trained and how it reads .wav files.

With everything set up, we moved on to developing the neural network. Since we were performing transfer learning, a complex neural network was unnecessary. In fact, after testing various configurations, the best results were achieved with a dense layer followed by a classification layer with a softmax activation function.

After completing the tests, we saved the model weights in .h5 format.

POSSIBLE IMPROVEMENTS:
As mentioned, obtaining the data was not an easy task. A potential improvement would be to expand the dataset. Instead of gathering new data (which was challenging), we could apply data augmentation or generate new sounds from the existing ones. For example, if we have 30 blender sounds, we could train a model capable of generating new blender sounds to enhance our dataset.

Nevertheless, we achieved good results in sound classification.
