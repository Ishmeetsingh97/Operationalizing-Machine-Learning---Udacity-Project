**Operationalizing Machine Learning**
* This project is about using and utilizing diverse functionally provided by Microsoft Azure Machine Learning tools.  This project uses the Bank Marketing Dataset. This dataset has been used to create a classification model to predict if the client will subscribe a term deposit or not using the AutoML feature in the Azure ML Studio.
Below is the architectural diagram for the workflow :

![alt text](link)

* This project performance can increase even more if the class imbalanced problem is solved. i.e Most datapoints in the response variable belong to one class and the availablity of predicting the minority class is very less as the data present to explain the minority class is very less. In the Bank Marketing dataset, this imbalanced class problem is present, 88.79%(29258/32950) datapoints belong to the class NO.

I am explaining the flow of the project below using the screesnshots captured while working on it:

1. Login to the azure portal, create a workspace for Machine Learing, Create an compute instance and an computer cluster and finally upload/select the dataset on which you want to perform the experiement.

![alt text](link)

2. Run the AutoML experiement by selecting the type of algorithms you want to run your dataset onto. i.e regression, classification, time series forecasting and select the best metrics that you want to optimize.

![alt text](link)

3. After the completion of the AutoML run, AutoML will give us a best performing algorithm with the primary metric selected at the previous step. Deploy that best performing model using Azure ML studio.

![alt text](link)

4. After the deployment of the model is completed, the Azure ML studio will provide a REST endpoint and two keys to authenticate that REST endpoint.

![alt text](link)

5. Run the logs.py files in the starter code to enable the Applications Insights

![alt text](link)

6. Download the config.json and the swagger.json files from the Azure ML studio. Run the serve.py and the swagger.sh to load the endpoint methods in swagger.

![alt text](link)

7. Using the the endpoint.py file provided in the starter code, edit that file to insert the REST endpoint link and the primary key crendentials to authenticate the endpoint. At this step a response will be received on based the JSON payload that has been sent to the Endpoint. 

![alt text](link)

8. Now, open the 'aml-pipelines-with-automated-machine-learning-step.ipynb' provided in the starter code to create a pipeline. Run the code until the last code block and run 'RunDetails(published_pipeline_run).show()' to view the details of the run.

![alt text](link)

7. Once the pipeline run is completed, Open the Azure ML link provided in the run details code block and publish the pipeline.

![alt text](link)
 

Video Demonstration link : 







