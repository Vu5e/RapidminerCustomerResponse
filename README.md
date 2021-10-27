# Prediction on Customer Response Sports Direct

## Business Understanding
- Responses of customer when offered gift for purchase of RM 500.
- Responses is a metric of how services offered by the company named Sports Direct meet customer expectations.
- Customers’ satisfaction plays a major role in retaining the customers.
- Evaluation of customer satisfaction is one good factor that helps in decision making strategy.
- Adopting suitable strategy  will results in increasing loyalty  which generates customers’ satisfaction.

## Analytical Question
- Does the customer response to the gift for purchase of RM 500 when offered?
- Customer response must be based on attributes example -
  - Sports
  - Lifestyles
  - Age
  - Earnings

## Objectives
- To construct suitable model to predict customer response towards the gift voucher of RM 500.
- To determine the performance of the Decision Tree, Random Tree and Naive Bayes in predicting customer towards the gift voucher of RM 500.

## Data Description
- Data Source - Final Assessment (Sports Direct)
- This dataset contains customer response towards the gift voucher survey.
- This data contain 9 attributes with 150,000 observations.

![image](https://user-images.githubusercontent.com/28688869/139120658-92414ba9-90b5-462b-b360-8819f9a9c126.png)

## Data Understanding
### List of Features
- Name
  - Names are used by random generate of characters and integer to protect the customer privacy.
- Age
  - Age are differ from teenagers to old age of retirement.
  - It differ from names.
- Lifestyle
  - Lifestyle are listed as cozily, healthy and active to indicate whether the customer daily lifestyles is.
- Zip Code
  - Zip Code are listed differently from each other customer.
- Family Status
  - Family status listed as single or married.
  - This to show whether they are married or single focusing on a healthy lifestyles.
- Car
  - Cars are listed differently with each other to indicate whether they are expensive or practical for them to use.
- Sports
  - Sports are what customer play mostly.
  - Listed as athletics, badminton and soccer.
- Earnings
  - Earnings is to show the annual earnings of customer which differ from each other.
- Label
  - This is the attribute to predict whether the customer is responding towards the gift purchase of RM 500.
  - Listed as no response and response.

### Passenger Sastifaction
- 47,400 customer responded towards the gift purchase.
- However, the other 102,600 customer do not response with the gift purchase.

![image](https://user-images.githubusercontent.com/28688869/139121120-c902fba1-508d-4104-a731-a7b7ee7a40e3.png)

## Data Preparation
### What kind of preparation?
- Putting the dataset inside for data preparation.

![image](https://user-images.githubusercontent.com/28688869/139121236-6800cb0e-041f-4d5d-93be-e1650a68d96c.png)

- No correlation value will have some problem as the data looks not clean.
- There’s no correlation value for sports and lifestyle.
- The attributes were removed.

![image](https://user-images.githubusercontent.com/28688869/139121437-01e4e145-c2a0-4f94-aeff-e5093d0c3728.png)

- Using “Select Attributes” operator.
- Excluded features
  - “lifestyle”
  - “name”
  - “sports”
  - “zip code”
- Attribute Filter Type Parameter will be “subset”

![image](https://user-images.githubusercontent.com/28688869/139121605-25f62f3f-907f-4ace-84d0-e7caed9ace50.png)

- Replacing features name.
- Using “Map” Operator to replace features name.
- Attribute filter type will be “single”.
- Chosen features will be “label”.
- Replacing features name of “response” to “responsive” and “non response” to “non responsive.

![image](https://user-images.githubusercontent.com/28688869/139121673-c6dc3727-ecbe-44d7-b3e6-a65715ebaf4a.png)

![image](https://user-images.githubusercontent.com/28688869/139121691-90f05619-abc4-44ee-9ff0-33a3f1932b60.png)

![image](https://user-images.githubusercontent.com/28688869/139121703-41f9b44d-7330-42b1-a80c-f63280aceb29.png)

- Replacing features name.
- Using “Map” Operator to replace features name.
- Attribute filter type will be “single”.
- Chosen features will be “car”.
- Replacing features name of “expensive” to “0” and “practical” to “1”.

![image](https://user-images.githubusercontent.com/28688869/139121775-337dd768-8c17-4ee4-97c3-a59c354f99db.png)

![image](https://user-images.githubusercontent.com/28688869/139121791-a9be83c7-07ad-4733-8f99-5d584f655e77.png)

- Replacing features name.
- Using “Map” Operator to replace features name.
- Attribute filter type will be “single”.
- Chosen features will be “family status”.
- Replacing features name of “single” to “0” and “married” to “1”.

![image](https://user-images.githubusercontent.com/28688869/139121832-da25da40-5f9f-48d7-bff6-0831bf293026.png)

![image](https://user-images.githubusercontent.com/28688869/139121847-ab9377c1-da64-489b-bdb8-022132cb5a10.png)

- Using the “Rename” operator to rename the label.
- Renaming from old name “label” to “response”.

![image](https://user-images.githubusercontent.com/28688869/139121904-17e15fcc-5e54-40ce-9a1e-f63dfffce08f.png)

![image](https://user-images.githubusercontent.com/28688869/139121916-1a26172f-503a-49a3-ac75-d36161db562e.png)

- Setting the roles.
- Using the “Set Role” operator to set the roles.
- In the “Parameter”, attribute name “response” will be chosen and target role will be “label”.

![image](https://user-images.githubusercontent.com/28688869/139121978-33d12a72-fa4a-4337-b1c1-21d026a869f5.png)

![image](https://user-images.githubusercontent.com/28688869/139122008-79974dbf-2fd5-4f56-a416-51780ea89aa3.png)

## Modelling
### Models Used
- Naive Bayes
- Random Tree
- Decision Tree

### Cross Validation
- The Cross Validation Operator is a Nested Operator with two subprocesses: a Training subprocess and a Testing subprocess. 
- The Training subprocess is used for training a model. In the Testing subprocess, the trained model is then applied. 
- The performance of the model is measured during the Testing phase.

### Naive Bayes
![image](https://user-images.githubusercontent.com/28688869/139122195-8be7398d-979f-4905-938f-8e7111bc1785.png)

### Random Tree
![image](https://user-images.githubusercontent.com/28688869/139122245-9b7b1043-b8ca-4a7e-a50b-52aec46a1ffb.png)

### Decision Tree
![image](https://user-images.githubusercontent.com/28688869/139122262-d21cacac-0da4-4c4a-8805-1fd70324312e.png)

## Evaluation
### ROC Curve
- Area under the ROC curve is a measure of model performance.
- Decision Tree has the best performance compared to Random Tree and Naive Bayes.
Area under the ROC curve is a measure of model performance.
Decision Tree has the best performance compared to Random Tree and Naive Bayes.

![image](https://user-images.githubusercontent.com/28688869/139122374-219056e2-9bc9-4375-9a7d-ee167379e501.png)

### Accuracy & Precision
- Recall or sensitivity gives us information about a model’s performance on false negatives (incorrect prediction of passengers who are satisfied).
- Precision gives us information of the model’s performance on false positives.
  - In this case, we may be far more concerned about having low false positives (low precision) than false negatives (recall).
  - What do we do with predicted not-responsive customers?
    - Improving the services offered e.g. online services for buying sports equipment and easier delivery or pick up in the store.
    - Offering different package then gift purchase e.g. sports equipments.

![image](https://user-images.githubusercontent.com/28688869/139122502-1cbf8ad8-a337-44b5-a8e5-5d59d4bc3237.png)

### Conclusion
- For non responsive customer towards the gift purchase, Sports Direct need to plan on bringing up ways to improve their response of the customer so they can retain and gain new one as well.
- Changing gift purchase to an object like sports equipment - gift purchase seems special but nowadays customer prefer something they can hold on to.
    - Sport Direct should consider giving special sports equipment such as branded one.
      - This would attract more customer to response towards the promotion.
      - This would retain customers and gain new customers as well with this promotion.
    - Sport Direct can also do something like sports day where they have multiple sports to do and encourage the customer or participant with special prizes.
      - This would increase the response towards the promotion as well.
