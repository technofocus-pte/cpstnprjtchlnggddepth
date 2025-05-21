# Challenge Part 1- Deploy Azure AI Fleet Resources

Objective  
Clone the project repo and run the setup script to deploy core Azure
resources for AI-powered fleet maintenance.

Steps**:**

1.  Clone the GitHub repo in Azure Cloudshell:

git clone https://github.com/

2.  Run below commands in cloud shell

> pip3 install --upgrade pip
>
> pip install azureml-sdk

3.  Provide permission (chmod +x setup.sh)to the setup.sh file located
    in contoso-fleet-ai folder and then run the setup script:

4.  Wait for the script to run completely( the script will take 15-20
    min to run successfully)

    - Azure Machine Learning Workspace

    - Azure Data Factory

    - Azure Database for PostgreSQL

    - Azure OpenAI (with GPT-Turbo model)

    - Azure AI Search

**Success Criteria:**

- Verify that all the required resources are deployed listed below are
  in the Azure portal.

  - Azure Machine Learning Workspace

  - Azure Data Factory

  - Azure Database for PostgreSQL

  - Azure OpenAI (with GPT-Turbo model)

  - Azure AI Search

- Verify that GPT-4.1model is deployed under Deployments in Azure AI
  Foundry portal.
