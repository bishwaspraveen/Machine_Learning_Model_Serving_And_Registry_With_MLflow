## Registering and Serving the optimized ML classification model (Logistic Regression) for Iris dataset with MLflow

### Step 1 : Choosing the best classification model based on comparing artifacts saved on MLflow and registering it.
![mlflow1](https://user-images.githubusercontent.com/79660080/215023584-b9d91683-2b0f-4dde-b131-7438f592a4e6.PNG)

### Step 2 : Productionizing the model that produces the best results.
![mlflow2](https://user-images.githubusercontent.com/79660080/215023634-e0aa8e1d-4b63-4e08-a07a-dc22a7141685.PNG)

### Step 3 : Serving the productionized model on MLflow server through `localhost://1234` and accesing the validation end point (`localhost://1234/invocations`) to generate output for a single test sample.
![mlflow3](https://user-images.githubusercontent.com/79660080/215023661-c14d5c44-e36e-4e8e-ba64-f30c0f759a2c.PNG)

### Step 4 : Accessing the server's endpoint (`localhost://1234/invocations`) to generate model output on a batch of test samples.
![mlflow4](https://user-images.githubusercontent.com/79660080/215023718-3faa336b-4afc-40ac-84ad-39b2b157dd93.PNG)

### Important commands to run MLflow in this set-up
#### 1. Command to use sqlite db connection to fetch data and project it onto MLFlow UI.
`mlflow server --backend-store-uri sqlite:///C:\Users\bishw\OneDrive\Desktop\Source_codes\Machine_Learning_Model_Life-Cycle_With_MLflow\Machine_Learning_Model_Registry_And_Serving\mlflow.db --default-artifact-root file:///C:\Users\bishw\OneDrive\Desktop\Source_codes\Machine_Learning_Model_Life-Cycle_With_MLflow\Machine_Learning_Model_Registry_And_Serving\artifacts`
#### 2. Command to start MLflow server on a random port of our choice.
`mlflow models serve --model-uri models:/iris-classifier/Production -p 1234 --no-conda`
