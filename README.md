# Speech-emotion-recognition-using-RNN

This repository contains a step-by-step guide along with the project files necessary to build a speech emotion recognition system from scratch. The user will start working with raw audio files from the RAVDESS database and use an RNN (LSTM) to train and test the model. The final step is to use the speech emotion recognition system in real-time, where the user will be able to use their own recorded speech and see the machine's emotion predictions in the form of emojis!

The project is divided into three steps (directories).

*Step 1*: Feature extraction\
*Step 2*: Model training and testing\
*Step 3*: Deploying the model

Please go to each directory in the order listed above and complete all the tasks before proceeding to the next.

The entire project was built using Python 3.0 (using Anaconda).

**Note:** Please wait till a cell finishes running before you run the next cell in the Jupyter notebooks. The cells need to run in the correct order for the project to work properly. If a cell is running, an hourglass icon will appear beside the file name on your browser's tab.

**Libraries**

Tensorflow v2.1.0
h5py v2.10.0
Scikit-learn v0.23.2
Librosa v0.8.0
Numba 0.48.0
Numpy v1.18.5
Pandas v1.1.1
Matplotlib v3.1.3

**Prerequisites**

1. *Install Python 3.0 in your machine*: I recommend downloading Anaconda distribution for your machine (Windows/Mac) and installing it. See the following link https://www.anaconda.com/products/individual

2. *Download the dataset in your machine*: The table below gives a short summary of the dataset we will be using for this project. Download the 'Audio_Speech_Actors_01-24.zip' file (208.5 MB) from this link https://zenodo.org/record/1188976#.YJ3tsKhKjIU and extract the zipped file inside a new directory, naming it "RAVDESS", in a disk in your machine which has at least 600 MB of space available.

| Corpus |  RAVDESS |
| :--- | :--- |
| Full Name | Ryerson Audio-Visual Database of Emotional Speech and Song |
| Origin | Ryerson University, Toronto, CA |
| Home URL | https://smartlaboratory.org/ravdess/ |
| License | Creative Commmons |
| Type | Multimodal |
| Speech Files | 1440 |
| Emotion Classes | 8 |
| Sentences | 2 |
| Male Actors | 12 |
| Female Actors | 12 |
| Total Actors | 24 |
| Age | 21 to 33 years |

*Filename Identifiers*:\
•	Modality (01 = full-AV, 02 = video-only, 03 = audio-only).\
•	Vocal channel (01 = speech, 02 = song).\
•	Emotion (01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised).\
•	Emotional intensity (01 = normal, 02 = strong). NOTE: There is no strong intensity for the 'neutral' emotion.\
•	Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door").\
•	Repetition (01 = 1st repetition, 02 = 2nd repetition).\
•	Actor (01 to 24. Odd numbered actors are male, even numbered actors are female).

3. *Create a new Python environment for this project*: It is recommended that you create a new environment for this project. That way, you won't overwrite the specific versions of the packages you already have in your current environment(s). However, if you don't mind installing everything in your current environment and potentially changing the library versions, you can skip this step. Use this link https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
