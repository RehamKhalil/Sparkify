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

# Reprosotry Desc
  1-mini_sparkify_event_data.7z: Fictious music streaming data provided by Udacity. This file is not available in the repository due to it's size.

  2-sparkify Udacity Capstone Project.ipynb : Exploratory notebook with all steps necessary to build a model that predicts churn for the Sparkify data.
