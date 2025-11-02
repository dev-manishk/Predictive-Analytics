# :books: Predictive Modelling for Telecom Churn Detection 
---



## :bulb: OUTCOMES / LEARNING
 In this practical, you learn how to:
* > Build a predictive model using historical customer data.
* > Identify customers who are likely to churn.
* > Apply data mining techniques to support customer retention.
* > Use IBM SPSS Modeler for modelling, filtering, prediction, and exporting results.

---

## :red_circle: Required Tools: 
* > IBM SPSS Modeler

---

## STEP-BY-STEP PROCEDURE: 

### :green_circle:  STEP 1: Import Training Dataset
* Open IBM SPSS Modeler → start a new stream.
* From Sources, drag an Excel Node into the workspace.
* Load telco x modeling data.xlsx → Click Apply → OK. 

   <img width="900" height="500" alt="image" src="https://github.com/user-attachments/assets/56ae6fbd-fdcc-4f8d-a756-88ce1fa5beed" />
---

### :green_circle: STEP 2: Filter Known Data
* Select the Excel Node → add a Select Node (Record Ops).
* Open it and set the condition:
  > data_known = "yes"
* Click Apply → OK.
  
   <img width="900" height="500" alt="image" src="https://github.com/user-attachments/assets/b453db07-da71-4b48-adc2-9b227c92ef9f" />
---

### :green_circle: STEP 3: View Filtered Records
* Attach a Table Node to the Select Node.
* Open the Table Node → adjust settings if needed → Apply → Run.

  <img width="900" height="500" alt="image" src="https://github.com/user-attachments/assets/9ef33a29-24b0-48a8-aaf7-6589bc31b21b" />
---

### :green_circle: STEP 4: Define Field Properties

* Select the Select Node and attach a Type Node.
* Open it → click Read Values to refresh measurement levels.
* Verify fields → Apply → OK.
* (Optional) Connect a Table Node to view updated field types.

  <img width="900" height="500" alt="image" src="https://github.com/user-attachments/assets/ae5517c5-50fc-4480-8bd4-17f76c8412f2" />
---

### :green_circle: STEP 5: Build the CHAID Model

* From Modeling, attach a CHAID Node to the Type Node.
* Open the CHAID Node and define roles:
 > Target: churn <br>
 > Predictors (Inputs): data_known, gender, age, handset
* Click Apply → OK → Run.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/4c9d5093-1bb9-4f54-9418-d9bceb204881" />
---

### :green_circle: STEP 6: Export Model Output

* Select the churn node → add a Table Node.
* Open → configure export options → Apply → Run to view results.

   <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/da209ae9-53b0-4442-bf4f-3a7210d53906" />
---

### :green_circle: STEP 7: Copy the Model for Deployment

* Right-click on the churn node → choose Copy Node.
* A duplicate churn node appears (dashed link to CHAID model).

   <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/81906372-b6da-41cf-8dab-5f9a62a62fc1" />
---

### :green_circle: STEP 8: Import Deployment Dataset
* Add a new Excel Node (Sources).
* Load telco x deployment data.xlsx → Apply → OK.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/23a0f1e8-ba2a-4e03-b689-38ee506fba2e" />
---

### :green_circle: STEP 9: Filter Deployment Data
* Attach a Select Node to the deployment Excel Node.
* Apply the condition:
> data_known = "yes"
* Apply → OK.
* Right-click the Select Node → Connect → link it to the copied churn model.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/4e29b544-a365-4f7b-8562-679190214d26" />
---

### :green_circle: STEP 10: Export Deployment Predictions
* Add a Table Node to the Select Node → Run to view predictions.
* Add another Table Node to the copied churn model → Run again to export predictions.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/28cc816b-d4de-451b-8a4d-8cc661cd9577" />
---

### :green_circle: STEP 11: Filter High-Risk Churn Customers
* Add another Select Node to the deployment Excel Node.
* Apply conditions:
> $R-churn = "Churned" and '$RC-churn'> 0.90
* Save with Apply → OK.
* Right-click the churn node → Connect → link it to this Select Node.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/29c6bd7b-0147-4685-afd4-d5a1c678a73c" />
---

### :green_circle: STEP 12: View High-Risk Output
* Attach a Table Node to this Select Node.
* Open → configure settings → Apply → Run.

 <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/dcb45b7d-21a0-4611-bfce-de797ceb3f72" />

---

### :green_circle: STEP 13: Remove Unwanted Fields
* Add a Filter Node to the Select Node.
* Open it → disable unnecessary fields.
* Click Apply → OK.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/97dd4f1a-f39a-4089-bc76-631828d5977f" />
---

### :green_circle: STEP 14: Export Final Clean Output
* Connect a Flat File Node (Export) to the Filter Node.
* Select the destination folder.
* Click Apply → Run to save the final output.
* (Optional) Rename the file to Output.

  <img width="920" height="500" alt="image" src="https://github.com/user-attachments/assets/35deada0-8caa-4d2b-bb53-8e62a88030c0" />

---
### Author 
* Name - Manish Kumar
* Course - Predictive Analytics
* Instructor: Mr. Ayushman Bhadauria


