# Challenge 4- Train and Deploy the Model via Azure ML Studio

**Objective**

Run the notebook to train a model to predict maintenance flag and deploy
it to an endpoint.

**Steps:**

1.  Open AML Studio

2. Clone the GitHub repo in Coputer instance terminal:

+++git clone https://github.com/technofocus-pte/TFFleetOptmztn.git+++

3.  Open **fleet_model_train.ipynb** from Notebooks section and run each cell of notebook

4. Update .env file with all your deployed Azure resource keys,endpoints
5. Train model using fleet_cleaned_data

7.  Deploy the model from notebook. Deployment takes 20-30 minutes
8.  Save the AML endpoint and API_Key values to use in challenge 7 while configuring chatapp

**Success Criteria:**

- AML model should have deployed successfully and endpoint and API key should have generated

- Predictions should display

![A screenshot of a chat AI-generated content may be incorrect.](./media/Ch4image1.jpg)

