1.) This prerequisite libraries must be installed first before running the notebooks
-sckit-learn
-numpy
-pandas
-pickle
-featurewiz
-ngboost
-statsmodels

2.) ProcessedDataCenterHall.csv is the initial dataset for this predictor. It will be pre-processed first via KDEclustering.ipynb where it determines the datapoints that will be used in feature_selection_frequency.ipynb to produce features.

a.) Open KDEclustering.ipynb In jupyter notebook
b.) Click Run All. 
c.) It will produce "main_dataset.csv"

3.) The newly produced "main_dataset.csv" will be used in feature_selection_frequency.ipynb. The said notebook is the one that resamples the main_dataset.csv files into 3 other time steps mainly hourly, daily, and 12-weekly. At the same time, this notebook is the one that produces features

a.) Open feature_selection_frequency.ipynb In jupyter notebook
b.) Click Run All. 
c.) It will produce "outputs_feature_select_cont.pickle" processed by featurewiz, a feature reduction technique
d.) It will also produce "ngboost_dataset.gz" which contains the 4 different time steps. It will be used by NGBoost and VARMAX

4.) NGBoost.ipynb is the one that implements NGBoost algorithm.

a.) Open NGBoost.ipynb In jupyter notebook
b.) Click Run All. 
c.) It will produce the performance metrics of the NGBoost algorithm.

5.) VARMAX.ipynb is the one that implements VARMAX algorithm.

a.) Open VARMAX.ipynb In jupyter notebook
b.) Click Run All. 
c.) It will produce the performance metrics of the VARMAX algorithm.