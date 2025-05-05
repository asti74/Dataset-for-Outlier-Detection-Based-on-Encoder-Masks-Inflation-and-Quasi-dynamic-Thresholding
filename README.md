# Dataset-for-Outlier-Detection-Based-on-Encoder-Masks-Inflation-and-Quasi-dynamic-Thresholding
Dataset for the paper "Outlier Detection for Cellular Networks Data Based on Encoder Masks Inflation and Quasi-dynamic Thresholding". It is distributed under the  Open Database License (ODbL) 1.0 as is the original dataset [A]. The following pre-processing was made before training the model:

The dataset from [A] was utilized and the following pre-processing was made before training the model:

- The 61 files corresponding to daily Human Telecommunication Activities (HTA) collected between November 1st 2013 and January 1st 2014 were downloaded from the multi-source urban dataset.
- 1% of the grids were randomly sampled for training and 1% for testing.
- The first 16 days from November 1 to 16 were selected for training.
- The values of the activities under the destination variable were regrouped into two categories – *Local* for destinations 0 or 39 (Italy country code) and *International* otherwise.
- The data was then averaged by *GridID*, *Destination* and 10-minute time blocks to reduce the effect of missingness in the data.
- The remaining missing data points in the Calls, SMS, and Internet variables were filled with zeros, assuming no data in the given grid and destination during the related 10-minute time block.
- All numerical continuous variables (Calls, SMSs, Internet) were normalized before being passed to the NN.

The processed data used for building the model is summarized as follows:

- *GridID* variable was treated as a categorical variable although recorded as numerical.
- *Timestamp* contains time blocks indicating the data recorded. A total of 8920 time blocks of 10 minutes each are recorded.
- *Destination* variable contains categorical variables with 2 values, Local and International.
- *SmsIn*, *SmsOut*, *CallIn*, *CallOut*, and *Internet* are all variables of interest used to detect outliers that contain continuous values.

**[A]** https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EGZHFV&version=1.3&selectTab=termsTab
DOI of the original paper: Barlacchi, G.; De Nadai, M.; Larcher, R.; Casella, A.; Chitic, C.; Torrisi, G.; Antonelli, F.; Vespignani, A.; Pentland, A.; Lepri, B. A multi-source dataset of urban life in the city of Milan and the Province of Trentino. Scientific Data 2015, 2, 1–15.


