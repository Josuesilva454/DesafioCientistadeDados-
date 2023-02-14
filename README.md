# DesafioCientistadeDados-

Dicionário dos dados

The dataset consists of 10 000 data points stored as rows with 8 features in columns:

1.	UID: unique identifier ranging from 1 to 10000
2.	product ID: consisting of a letter L, M, or H for low (50% of all products), medium (30%) and high (20%) as product quality variants and a variant-specific serial number
3.	type: just the product type L, M or H from column 2
4.	air temperature [K]: generated using a random walk process later normalized to a standard deviation of 2 K around 300 K
5.	process temperature [K]: generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K.
6.	rotational speed [rpm]: calculated from a power of 2860 W, overlaid with a normally distributed noise
7.	torque [Nm]: torque values are normally distributed around 40 Nm with a SD = 10 Nm and no negative values.
8.	tool wear [min]: The quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process.

A 'machine failure' label that indicates whether the machine has failed in this particular datapoint for any of the following failure modes is true.
The machine failure consists of five independent failure modes:
1.	tool wear failure (TWF): the tool will be replaced of fail at a randomly selected tool wear time between 200 - 240 mins (120 times in our dataset). At this point in time, the tool is replaced 69 times, and fails 51 times (randomly assigned).
2.	heat dissipation failure (HDF): heat dissipation causes a process failure, if the difference between air- and process temperature is below 8.6 K and the tools rotational speed is below 1380 rpm. This is the case for 115 data points.
3.	power failure (PWF): the product of torque and rotational speed (in rad/s) equals the power required for the process. If this power is below 3500 W or above 9000 W, the process fails, which is the case 95 times in our dataset.
4.	overstrain failure (OSF): if the product of tool wear and torque exceeds 11,000 minNm for the L product variant (12,000 M, 13,000 H), the process fails due to overstrain. This is true for 98 datapoints.
5.	random failures (RNF): each process has a chance of 0,1 % to fail regardless of its process parameters. This is the case for only 5 datapoints, less than could be expected for 10,000 datapoints in our dataset.

Ide#
install Jupyter Notebook 

pip install pandas
#
pip install numpy
#
pip install IPython
#
pip install plotly
#
pip install importlib
#
pip install matplotlib
#
pip install pytest-warnings
#
pip install pandas-profiling
#
pip install  scikit-learn 
#
pip install statsmodels 
#
pip install imblearn
