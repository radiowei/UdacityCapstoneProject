# San Francisco Bay Area Bike Sharing Data Analysis

This project is to investigate a docked bike-sharing system in San Francisco Bay Area, data collected during 2013-2015 when this system just got launched. Two major questions will addressed:
1. Can we predict the number of trips in a future date?
2. Can we find some unique patterns for non-subscribers?

## Getting Started

The original data can be downloaded from here: 
https://www.kaggle.com/benhamner/sf-bay-area-bike-share/downloads/sf-bay-area-bike-share.zip.

The size of original data is 660MB when downloaded and about 5GB when unzipped.

### Prerequisites

Hardware: GPU is required to run some of the codes. 

Environment: 
Ubuntu 16.04.3 LTS
Python 3.6.4.

Important Python packages:
numpy: 1.13.3
scipy: 1.0.0
pandas: 0.21.1
matplotlib: 2.1.1
sklearn: 0.19.1
xgboost: 0.6
tensorflow: 1.4.1
keras: 2.1.2

Other used Python packages:
sqlite3, re, mglearn, tqdm, gmplot, pandas\_ml, pydotplus, time, datetime, bdateutil, holidays, more_itertools, random, wurlitzer, warnings, socket, sys.

### Installing

Most of the Python packages can be installed by "pip install package-name". A few needs special installation:

* Install xgboost with GPU functionality. Follow the instructions below:
https://gist.github.com/persiyanov/1d5499fd10802fa309d803359039a93b
https://xgboost.readthedocs.io/en/latest/build.html#python-package-installation

Briefly:
====================================================================
sudo apt-get install git make g++ python-setuptools
git clone --recursive https://github.com/dmlc/xgboost
cd xgboost
make -j4
cd python-package
sudo python setup.py install

Last command can raise exception ImportError: No module named numpy.distutils.core. Whatever, XGBoost is correctly installed. Only thing we need is to add the package to PYTHONPATH:

echo "export PYTHONPATH=~/xgboost/python-package" > ~/.bash_profile
source ~/.bash_profile
====================================================================

* Install tensorflow-gpu: 
To use tensorflow-gpu as the backend of the Keras, install Keras first and then "pip install tensorflow-gpu".

* Install Graphviz: sudo apt-get install graphviz

Also "pip install graphviz" for xgboost
https://www.howtoinstall.co/en/ubuntu/xenial/graphviz

## Running the code

Running through the whole Jupyter notebook takes about 105 minutes on my computer.
For the first run, set the sql\_status to True. After that, the sql\_status can be set to False to reduce the running time.

## Authors

**Zhiwei Lin** 

This document is created following the template here:
https://gist.github.com/PurpleBooth/109311bb0361f32d87a2#file-readme-template-md
