# Deterministic and probabilistic forecasting of wind power generation and ramp rate with expectation-implemented deep learning
Codes for "Deterministic and probabilistic forecasting of wind power generation and ramp rate with expectation-implemented deep learning."

  ## 0. Dataset
  We used publicly available data from ERCOT for the training and test data on wind power generation and ramp rate. The dataset contains the hourly aggregated wind and solar power output for ERCOT from 2020 to 2023 and is included as the .csv files. 
  For additional information, see https://www.ercot.com/mp/data-products/data-product-details?id=PG7-126-M.
  
  ## 1. Basic Daily Forecasting
  Numbers in the .ipynb files represent the order of the proposed forecasting algorithms. You can skip files #1 and #2 by using the .h5 files and directly go to File #3.
  ### Brief description of each code
  1. Generation Forecasting.ipynb
    - Code for wind power generation forecasting. The results are "Basic Model Final.h5" and "Error Learning Model.h5" files.
  2. Ramp Rate Forecasting.ipynb
    - Code for wind power ramp rate forecasting. The results are "Basic Ramp Model Final.h5" and "Error Learning Ramp Model.h5" files.
  3. Getting Forecasting Results from the Pretrained Models.ipynb
    - This file simultaneously gives generation and ramp rate forecasting results using the results from files #1 and #2.
  4. Combining Two Forecasting Results.ipynb
    - This file integrates two heterogeneous generation and ramp rate forecasting results into a unified forecasting result.
  5. Probabilistic Forecasting.ipynb
    - Code for the probabilistic forecasting of the wind power ramp rate based on the combined results from file #4.
  6. Plotting for Deterministic Forecasting.ipynb
    - Simple statistics for the wind power generation and ramp rate dataset. Simple figure generation for signal attributes and loss histories.
  7. Plotting for Probabilistic Forecasting.ipynb
    - Figure generation for the process of the proposed probabilistic forecasting method.
  8. Independency Analysis.ipynb
    - HSIC test results to evaluate the independency between wind power generation and ramp rate.

  ## 2. SVD Test
  Compare the models with and without SVD-based feature generation.
  ## 3. Ablation Test
  Ablation test results about DNN strategies, including attention block, output block, Positive-Negative (P-N) residual network, and PReLU activation function.
  ## 4. Forecasting Error Indices
  Compare models trained by MSE, MAE, and proposed error function (MAEMS and MAEMD).
  ## 5. Different Forecasting Horizon
  Forecasting results with different forecasting horizons, such as 1-h, 6-h, 12-h ahead wind power forecasting.
  ## 6. SOTA Comparison & Shuffling
  Comparison of the proposed model with Transformer, Informer, N-Beats, SCINet, SegRNN, and PatchMixer models. Furthermore, impact of shuffling the training dataset is also tested.
