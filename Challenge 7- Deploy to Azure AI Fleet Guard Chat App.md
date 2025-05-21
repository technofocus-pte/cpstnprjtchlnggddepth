# Challenge 7: Deploy Azure AI Fleet Guard Chat App

**Objective**

Deploy Azure AI Fleet Guard app as Web app in Azure.

**Steps:**

1.  Install Azute Tool kit in VS code

2.  Sign in with your azure subscription in VS code

3.  Create the web app with the name(**FleetGuard**) and select Python
    10.0 as environment

4.  Deploy the chat app as Web app in Azure.

5.  in Azure portal, web app add below environment variables.

[TABLE]

6.  Add startup command as -\> **python -m flask run --host=0.0.0.0
    --port=8000** in configuration section of the app.

7.  Add Microsoft as identity provider with application-read and write
    permissions

8.  Set System assigned identity ON

9.  Access the app and check the response of the app with below prompts.

> Vehicle 98765 has an engine health of 82.6%. Coolant temperature is
> high (113°C)
>
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
>
> ![A screenshot of a chat AI-generated content may be
> incorrect.](./media/image1.png)

**Success Criteria:**

- App should respond with correct tips and cost for the repairs
