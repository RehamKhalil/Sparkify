# Sparkify Project
This project is the final Capstone project of the Udacity Data Scientist Nanodegree program. The aim is to learn how to manipulate realistic datasets with Spark to engineer relevant features for predicting churn. Input data is related to the fictive music streaming service Sparkify (similar to Spotify and Pandora).

# Installation
The code should run with no issues using Python versions 3. See the requirements.txt file for details about library versions.

# Libraries 
import pandas as pd
import matplotlib.pyplot as plt
import matplotlib.gridspec as grd
import warnings
import seaborn as sns
import datetime
from time import time

import pyspark
import pyspark.sql.functions as F
from pyspark import SparkConf
from pyspark.sql import SparkSession
from pyspark.sql.functions import udf, col, isnan, when, count
from pyspark.sql.types import IntegerType, LongType

from pyspark.ml.feature import StringIndexer, VectorAssembler, MinMaxScaler
from pyspark.ml import Pipeline
from pyspark.ml.classification import LogisticRegression
from pyspark.ml.classification import DecisionTreeClassifier
from pyspark.ml.classification import RandomForestClassifier
from pyspark.ml.classification import NaiveBayes
from pyspark.ml.tuning import CrossValidator, ParamGridBuilder
from pyspark.ml.evaluation import BinaryClassificationEvaluator, MulticlassClassificationEvaluator

from pyspark.mllib.evaluation import MulticlassMetrics
