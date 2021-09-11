# A CNN-LSTM-based Method for Stock Prediction

## Note About Provided Notebooks
The directory `script` will contain 3 notebooks.<br>
The reason is that two scripts were used to train different models. One on my private computer, the other one on a server hosted by HTW Berlin.<br>
For convenience, both scripts were merged into one, called `CNN_LSTM_merged.ipynb`.<br>
The two separate scripts which were merged can be found in `script/separated`.<br>
The merged script `CNN_LSTM_merged.ipynb` should be used over the separated ones as `script/separated/CNN_LSTM_2.ipynb` would not be able to execute on its own due to missing methods from the other notebook.

## How To Get The Data
The raw data used for training the model can be downloaded from <br>
https://drive.google.com/drive/folders/1zcOdn3t8ES9F42JDPknc9LFIwml5Bkeb?usp=sharing 
### Get The Data Into Appropriate Form for Training
In order to be able to work with the data, please download the csv files (if necessary) and move them into the folder `data/raw`.<br>
Next, the notebook `CNN_LSTM_merged.ipynb` in the directory `script` can be run. Make certain to initialise all cells leading to the method `process_data`.<br>
The cell defining the method `process_data` contains further information on which variable defines the output directory and which parameters can be passed to the preprocessing method.<br>
<em>Note that the method invocation of `process_data` is commented out at the bottom of its cell. And needs to be uncommented and specified to normalizing data or not normalizing it.</em>
### Available Processed Data in Project Folder
There is already data available which is processed in the directory `data/samples`. However, this holds only data from 50 stocks as having all stocks in this project uploaded would take up too much space. Hence, the link to the raw data in form of csv files.

## Slides And Charts From The Presentation
The powerpoint presentation which contains all plots for the experiments can be found in the directory `presentation`.

## Location of Log Files And Serialised Models For Plotting
Logging files for each experiment as well as saved models or tensorboard directories can be found in the directory `logs`.<br>
Data is devided into one part which contains results for the papers LSTM model (directory `logs/lstm`) and the other one contains results for the CNN extensions of the LSTM model (directory `logs/cnn_lstm`).

## View Tensorboard Summaries
To view created graphs from Tensorboard, you need to navigate in the terminal to `cd data/samples`. From there, run the command `tensorboard --logdir=runs`.<br>
Make certain that you do not have more than one summary folder (`train_*`) in the `runs` directory as this would cause errors in displaying the summaries.

## Sources
LSTM-based stock prediction research paper:<br>
https://ieeexplore.ieee.org/abstract/document/7364089 <br>
CNN paper which points out the necessity of leaky relu as activation function for CNNs:<br>
https://iopscience.iop.org/article/10.1088/1757-899X/435/1/012026/pdf<br>
Implementation design for training and validation methods combined with plotting:<br>
https://pythonprogramming.net/analysis-visualization-deep-learning-neural-network-pytorch/?completed=/gpu-deep-learning-neural-network-pytorch/
