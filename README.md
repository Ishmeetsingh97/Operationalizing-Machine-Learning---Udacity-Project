**Operationalizing Machine Learning**
* This project is about using and utilizing diverse functionally provided by Microsoft Azure Machine Learning tools.  This project uses the Bank Marketing Dataset. This dataset has been used to create a classification model to predict if the client will subscribe a term deposit or not using the AutoML feature in the Azure ML Studio.
Below is the architectural diagram for the workflow :

![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/diagram.png)

* This project performance can increase even more if the class imbalanced problem is solved. i.e Most datapoints in the response variable belong to one class and the availablity of predicting the minority class is very less as the data present to explain the minority class is very less. In the Bank Marketing dataset, this imbalanced class problem is present, 88.79%(29258/32950) datapoints belong to the class NO.

I am explaining the flow of the project below using the screesnshots captured while working on it:

1. Login to the azure portal, create a workspace for Machine Learing, Create an compute instance and an computer cluster and finally upload/select the dataset on which you want to perform the experiement. <br />
**(Rubric Point Screenshot : “Registered Datasets” in ML Studio shows "Bankmarketing" dataset available)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_1.png)

2. Run the AutoML experiement by selecting the type of algorithms you want to run your dataset onto. i.e regression, classification, time series forecasting and select the best metrics that you want to optimize.
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/Screenshot%20from%202020-09-29%2021-28-03.png)

3. After the completion of the AutoML run, AutoML will give us a best performing algorithm with the primary metric selected at the previous step. Deploy that best performing model using Azure ML studio.<br />
**(Rubric Point Screenshot : The experiment is shown as completed.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_2.png)
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_3.1.png)
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_3_2.png)


4. After the deployment of the model is completed, the Azure ML studio will provide a REST endpoint and two keys to authenticate that REST endpoint.<br />
**(Rubric Point Screenshot : Endpoints section in Azure ML Studio, showing that “Application Insights enabled” says “true”.)**

![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_4.png)
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/Screenshot%20from%202020-09-29%2021-32-04.png)


5. Run the logs.py files in the starter code to enable the Applications Insights.<br />
**(Rubric Point Screenshot : Logging is enabled by running the provided logs.py script.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_5.png)

6. Download the config.json and the swagger.json files from the Azure ML studio. Run the serve.py and the swagger.sh to load the endpoint methods in swagger.<br />
**(Rubric Point Screenshot : Swagger runs on localhost showing the HTTP API methods and responses for the model.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_6.1.png)
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_6.png)

7. Using the the endpoint.py file provided in the starter code, edit that file to insert the REST endpoint link and the primary key crendentials to authenticate the endpoint. At this step a response will be received on based the JSON payload that has been sent to the Endpoint. 


![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_7.1.png)
**(Rubric Point Screenshot : endpoint.py script runs against the API producing JSON output from the model.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_7.png)


8. Now, open the 'aml-pipelines-with-automated-machine-learning-step.ipynb' provided in the starter code to create a pipeline and sumbit it to run.<br />
**(Rubric Point Screenshot : The pipeline section of Azure ML studio, showing that the pipeline has been created.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_8.png)
**(Rubric Point Screenshot : The Bankmarketing dataset with the AutoML module.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_9.png)


9. Run the code until the last code block and run 'RunDetails(published_pipeline_run).show()' to view the details of the run.<br />
**(Rubric Point Screenshot : A screenshot of the Jupyter Notebook is included in the submission showing the “Use RunDetails Widget” with the step runs.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_11.png)
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_11.1.png)


10. Once the pipeline run is completed, Open the Azure ML link provided in the run details code block and publish the pipeline which will give an endpoint and show status as active.<br />
**(Rubric Point Screenshot : The “Published Pipeline overview”, showing a REST endpoint and a status of ACTIVE.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_screenshot_10.png)
 
11. Showing REST pipeline endpoint as Active in ML Studio. <br />
**(Rubric Point Screenshot : ML studio showing the scheduled run.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_Screenshot_15.png)
**(Rubric Point Screenshot : ML studio showing the pipeline endpoint as Active.)**
![alt text](https://github.com/Ishmeetsingh97/Operationalizing-Machine-Learning---Udacity-Project/blob/master/screenshots/required_Screenshot_16.png)

Video Demonstration link : https://drive.google.com/file/d/1NR5QJlrw7992tQt2283vbfGgqDbIxh-l/view?usp=sharing







