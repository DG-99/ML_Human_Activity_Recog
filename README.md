Heterogeneity_Acivity_Recognition_in_Humans
===

[Dataset Link](https://archive.ics.uci.edu/ml/datasets/Heterogeneity+Activity+Recognition)
---

Libraries used:
---
Numpy, Pandas, Scikit_learn, Matplotlib and Keras

File Structure:
---
The project has 9 main files: 4 for data management and 4 for Machine Learning codes and 1 for plotting results.

Data management files:
---
1. The huge dataset (~1.4GB) was partitioned into 13 files and the script 'compressed_file.py' and 'compress2.0.py' were used to downsample the dataset stored in these 13 files to obtain 13 compressed files.

2. The scripts 'merge.py' and 'merge2.0.py' were used to merge the compressed files to obtain the dataset which was used for training. The 2.0 scripts were used for merging the accelerometer and gyroscope data.

Machine Learning files:
---
1. "main_neural_network.py" contains the Neural Network implementation which was used seperately on gyroscope data and accelerometer data.

2. "main_RNN.py" contains Long short-term memory(LSTM) implementation which was used on both, the merged data and the accelerometer and gyroscope data seperately.

3. "main.py" takes the complete dataset (not the compressed dataset) and implements LSTM.

4. "PreprocessedData.py" takes in the [dataset](https://archive.ics.uci.edu/ml/datasets/Smartphone-Based+Recognition+of+Human+Activities+and+Postural+Transitions) and outputs the result, this file was mainly created to see whether our LSTM model was good enough (The accuracy obtained from this preprocessed dataset was 91%).

Plotting:
---
Used for plotting the result obtained from "main_NN.py"

Model:
---
"model.h5" stores the final model to the problem.


NOTE:
Final code is run by 'main.py' and for this the dataset must be in the same folder and run the script using python3
