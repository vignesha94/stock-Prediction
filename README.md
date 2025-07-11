**Stock Price Prediction using Hybrid BiLSTM with Technical Indicators**
**Overview**
This project implements a hybrid Bidirectional LSTM (BiLSTM) model enhanced with technical indicators for predicting stock prices in the Indian market. The model processes historical OHLC (Open, High, Low, Close) data combined with technical indicators like SMA, EMA, RSI, and ATR to forecast future stock prices. The pipeline includes data extraction, preprocessing, feature engineering, model architecture, training, and evaluation.

**Key Features**
Data Processing: Extraction and cleaning of historical stock data from multiple sectors (Gold, NIFTY indices, VIX)

**Feature Engineering: Calculation of technical indicators:**

Simple Moving Average (SMA)

Exponential Moving Average (EMA)

Relative Strength Index (RSI)

Average True Range (ATR)

Hybrid Model Architecture: Combines sequence processing (BiLSTM) with technical indicator inputs

Custom Data Handling: Special processing for different data types (e.g., Gold prices)

Training Pipeline: Complete workflow from data preparation to model training

**Requirements**
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow nltk yfinance

**Data Preparation**
The dataset includes historical Indian stock data from multiple sectors (1990-2022). The preprocessing pipeline:

Extracts data from ZIP archives

Standardizes date formats and column names

Handles missing values with forward/backward filling

Adds technical indicators

Merges data from all sectors into a unified dataset

**Model Architecture**

**Key components:**

Bidirectional LSTM layers for sequence processing

Dense layers for technical indicator processing

Concatenation of both feature streams

Dropout layers for regularization

Adam optimizer with MSE loss

**Usage**
Run the Jupyter notebook _Stock_Prediction_TechBiLSTM.ipynb_

The notebook will:

Process raw stock data

Compute technical indicators

Train the hybrid BiLSTM model

Evaluate performance

Generate training loss plots

**Results**
The model shows decreasing training and validation loss over 100 epochs. Key evaluation metrics include:

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

R-squared (R²)

**File Structure**
_Stock_Prediction_TechBiLSTM.ipynb:_ Main implementation notebook

_merged.csv:_ Processed dataset (generated after running the notebook)

_README.md:_ This documentation file
