This example uses:

- Only ONE DMN Decision table is used (3 inputs, 1 output).

- 12 decision rules - It is only possible to identify ONE output value according to the defined inputs. This represents a Hit Policy UNIQUE (U).
  > Existing Customer:"True", Risk Score:<=120, Credit Score:<590, Decision:"HIGH"
  > Existing Customer:"True", Risk Score:<=120, Credit Score:[590..610], Decision:"MEDIUM"
  > Existing Customer:"True", Risk Score:<=120, Credit Score:>610, Decision:"LOW"
  > Existing Customer:"True", Risk Score:>120, Credit Score:<600, Decision:"HIGH"
  > Existing Customer:"True", Risk Score:>120, Credit Score:[600..625], Decision:"MEDIUM"
  > Existing Customer:"True", Risk Score:>120, Credit Score:>625, Decision:"LOW"
  > Existing Customer:"False", Risk Score:<=100, Credit Score:<580, Decision:"HIGH"
  > Existing Customer:"False", Risk Score:<=100, Credit Score:[580..600], Decision:"MEDIUM"
  > Existing Customer:"False", Risk Score:<=100, Credit Score:>600, Decision:"LOW"
  > Existing Customer:"False", Risk Score:>100, Credit Score:<590, Decision:"HIGH"
  > Existing Customer:"False", Risk Score:>100, Credit Score:[590..615], Decision:"MEDIUM"
  > Existing Customer:"False", Risk Score:>100, Credit Score:>615, Decision:"LOW"

- The decision table does not include "wild cards" in its attributes (See Figure DMNDecisionTable_Example-1)

- Currently the implemented chatbot has a value of lifespan =4. That is, after the fourth interaction with the chatbot, the context is no longer active and the value of the parameters could be lost, generating an unexpected response. This value can be modified in the index.js file 

LINK TO THE CHATBOT WEB ACCESS:
  - DMNChatbotExample1 - RiskCategory:
  - https://bot.dialogflow.com/DMNChatbotExample1

LINK TO THE EVALUATION QUESTIONNAIRE:
  - DMNChatbotExample1 - RiskCategory:
  - https://forms.gle/z9TCdCWas4vKrkvf6