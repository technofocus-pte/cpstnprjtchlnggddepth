# Challenge 6 - Run the Azure AI Fleet Chat App locally

**Objective**

Run the AI chat assistant that pulls answers from vector search and
fleet predictions.

**Steps:**

1.  Edit .env with your values in app folder of Github repo

2.  Run below below dependencis in terminal.

> pip install openai==0.28
>
> python.exe -m pip install --upgrade pip
>
> pip install -r requirements.txt
>
> python -m pip install --user -r requirements.txt
>
> pip install openai\[datalib\]

3.  Run the app locally with the command below

**python app.py**

![A screenshot of a computer AI-generated content may be
incorrect.](./media/image1.png)

4.  Check app response with any of below prompts

> my vehicle - 98765 has enginehealth - 0.826120
>
> Predict maintenance issues for my vehicle with 80,000 km mileage
>
> Will my car overheat based on engine temperature 90°C?
>
> vehicle 24353 's enginehealth is 0.9 and vehicle sensor speed is 101
>
> *What should I do if my engine health is below 0.5?*
>
> *What are 3 signs my fleet needs urgent servicing?*

**Success Criteria:**

- App should respond with correct tips and cost for the repairs
