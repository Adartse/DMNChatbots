This example uses:

- Only ONE DMN Decision table is used (3 inputs, 1 output).

- 8 decision rules - It is only possible to identify ONE output value according to the defined inputs. This represents a Hit Policy UNIQUE (U).
  > Existing Customer:"True", Risk Score:<=120", Credit Score:"-", Decision:"LOW"
  > Existing Customer:"True", Risk Score:>120", Credit Score:<600, Decision:"HIGH"
  > Existing Customer:"True", Risk Score:>120", Credit Score:[600..625], Decision:"MEDIUM"
  > Existing Customer:"True", Risk Score:>120", Credit Score:>625, Decision:"LOW"
  > Existing Customer:"False", Risk Score:<=100", Credit Score:<580, Decision:"HIGH"
  > Existing Customer:"False", Risk Score:<=100", Credit Score:[580..600], Decision:"MEDIUM"
  > Existing Customer:"False", Risk Score:<=100", Credit Score:>600, Decision:"LOW"
  > Existing Customer:"False", Risk Score:>100", Credit Score:-, Decision:"HIGH"

- The decision table includes "wild cards" in one of its attributes (See Figure DMNDecisionTable_Example-2)

- Currently the implemented chatbot has a value of lifespan =4. That is, after the fourth interaction with the chatbot, the context is no longer active and the value of the parameters could be lost, generating an unexpected response. This value can be modified in the index.js file

LINK TO THE CHATBOT WEB ACCESS:
  - DMNChatbotExample2 - RiskCategory:
  - https://bot.dialogflow.com/DMNChatbotExample2

LINK TO THE EVALUATION QUESTIONNAIRE:
  - DMNChatbotExample2 - RiskCategory:
  - https://forms.gle/xJV7JCDxu2GMHPm19