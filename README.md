# Build an AI product recommendation engine for an online store

## Demo

An end-to-end project on creating the below product recommendation engine for an online store for different products.

![](https://github.com/Abeer-Haroon/Build-an-AI-powered-product-recommendation-engine/blob/master/images/pixieApp.gif)

## Prerequisites

1. Sign up for an [IBM Cloud account](https://cloud.ibm.com/registration/).
2. Download or Clone this repo.

## Estimated time

This tutorial takes about 20 minutes to complete if you already have an IBM cloud account set up.

## Steps

1. Create an instance of the Watson Machine Learning
   - Go to the [Watson Machine Learning]( https://cloud.ibm.com/catalog/services/machine-learning) page in the IBM Cloud Catalog.
   - Click **Create**.
   
 2. Create an instance of the Cloud Object Storage
   - Go to the [Cloud Object Storage](https://cloud.ibm.com/catalog/services/cloud-object-storage) page in the IBM Cloud Catalog.
   - Click **Create**.
  
3. Create an instance of the Watson Studio
   - Go to the [Watson Studio](https://cloud.ibm.com/catalog/services/watson-studio?bss_account=e366b6e4fb004c5eaccfbe7042b670a4) page in the IBM Cloud Catalog.
   - Click **Create**.

![](https://github.com/Abeer-Haroon/AI-Treasure-Hunt-With-Watson/blob/master/images/ath12.png)

   - Click **Get Started**.
 
   - Click **Create a Project** > Standard

   - Name the project. Select **Storage** > cloud object storage. **Create**
   
 3. Upload the Dataset: customers_orders_history.csv

![](https://github.com/Abeer-Haroon/Predicting-monthly-demand-of-items/blob/master/images/upload.png)

4. Open the dataset. Click on **Refine** to cleanse and shape it. 

5. Remove the unnecessary columns: CUSTNAME, NATIONALITY, and ORDER_ID as shown below.

![](https://github.com/Abeer-Haroon/Build-an-AI-powered-product-recommendation-engine/blob/master/images/DR1.gif)

6. Remove the missing values from the column: CUST_ID

   Select the 3 dots on the column > Remove missing values.

7. Select the right data type for CUST_ID as shown below.

![](https://github.com/Abeer-Haroon/Build-an-AI-powered-product-recommendation-engine/blob/master/images/DR2.gif)

8. Upload the notebook 'wml-product-recommendation-aiengine.ipynb' to the project.

![](https://github.com/Abeer-Haroon/Build-an-AI-powered-product-recommendation-engine/blob/master/images/notebook1.gif)

9. Open the notebook. Add the credentials of your Watson Machine Learning service in **4.1**.

``` 
   wml_credentials = {
     "apikey": "***",
     "iam_apikey_description": "Auto-generated for key ***",
     "iam_apikey_name": "Service credentials-1",
     "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Writer",
     "iam_serviceid_crn": "crn:v1:bluemix:public:iam-identity::a/***",
     "instance_id": "***",
     "url": "https://us-south.ml.cloud.ibm.com"
   }
   
   
``` 

10. Run all the cells in the notebook to create the model. Test your model with the Pixie App at the end of the notebook. 

    Voilà! You're done creating your own AI recommendation engine!!






