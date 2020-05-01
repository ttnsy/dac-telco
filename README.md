# Data Analysis Capstone

This is developed as one of Algoritma Academy Data Analytics Specialization using capstone Projects. The deliverables of this project is a simple analytic dashboard using Flask framework.

## Rubrics

...

---

## Environment Setup

There are few prerequisites needed for this project. Usually, we can use `pip install`/`conda install` to install requirements on our environment. But for now, let's try on another approach on preparing libraries needed for a certain project.

If you browse on `/assets` directory on this repository, you'll find a file called `requirements.txt`. This file is used for specifying what python packages are required to run a certain project. If you open up the file, you will see something that looks similar to this:

backcall==0.1.0  
certifi==2019.11.28  
chardet==3.0.4  
cycler==0.10.0  
decorator==4.4.0  
idna==2.9  
ipython==7.7.0  
......


Notice we have a line for each package, then a version number. This is important because as you start developing your python applications, you will develop the application with specific versions of the packages in mind. In simple, `requirements.txt` helps to keep track of what version of each package you are using to prevent unexpected changes.

Run the following command to create a new conda environment from requirements.txt:

**Step 1**: Prepare a "blank" new environment and activate it

```
conda env create -n <ENV_NAME> python=<PYTHON_VERSION>
conda activate <ENV_NAME>
```

**Step 2**: Navigate to the folder with your `requirements.txt`

```
cd <PATH_TO_REQUIREMENTS>
```

**Step 3**: Install the requirements

```
pip install -f requirements.txt
```

You have now successfuly installed all the requirements needed on this project! For your convenience, don't forget to link your new environment to jupyter-notebook using kernel:

```
pip install ipykernel
python -m ipykernel install --user --name=<ENV_NAME>
```
---

## Dataset

The data set is taken from IBM sample data sets for telco customer retention programs in [Kaggle](https://www.kaggle.com/blastchar/telco-customer-churn). Each row represents a customer, each column contains customer’s attributes described on the column Metadata.

The data set includes information about:

- **Customers who left within the last month** – the column is called Churn
- **Services that each customer has signed up for** – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.
- **Customer account information** – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
- **Demographic info about customers** – gender, age range, and if they have partners and dependents

### Data Glossary

- `customerID`: Customer ID
- `gender`: Whether the customer is a male or a female
- `SeniorCitizen`: Whether the customer is a senior citizen or not (1, 0)
- `Partner`: Whether the customer has a partner or not (Yes, No)
- `Dependents`: Whether the customer has dependents or not (Yes, No)
- `tenure`: Number of months the customer has stayed with the company
- `PhoneService`: Whether the customer has a phone service or not (Yes, No)
- `MultipleLines`: Whether the customer has multiple lines or not (Yes, No, No phone service)
- `InternetService`: Customer’s internet service provider (DSL, Fiber optic, No)
- `OnlineSecurity`: Whether the customer has online security or not (Yes, No, No internet service)
- `OnlineBackup`: Whether the customer has online backup or not (Yes, No, No internet service)
- `DeviceProtection`: Whether the customer has device protection or not (Yes, No, No internet service)
- `TechSupport`: Whether the customer has tech support or not (Yes, No, No internet service)
- `StreamingTV`: Whether the customer has streaming TV or not (Yes, No, No internet service)
- `StreamingMovies`: Whether the customer has streaming movies or not (Yes, No, No internet service)
- `Contract`: The contract term of the customer (Month-to-month, One year, Two year)
- `PaperlessBilling`: Whether the customer has paperless billing or not (Yes, No)
- `PaymentMethod`: The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
- `MonthlyCharges`: The amount charged to the customer monthly
- `TotalCharges`: The total amount charged to the customer
- `Churn`: Whether the customer churned or not (Yes or No)