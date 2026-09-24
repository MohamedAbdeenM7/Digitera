# Meridian Health Dataset — Data Cleaning

A Python-based data cleaning project developed as part of the **Digitera Program | Data Analysis Track**.

The project focuses on cleaning and standardizing the Meridian Health dataset using **Python and pandas**, combining sales data, enriching it with product cost information, cleaning customer records, and creating useful financial metrics.

## 📌 Project Overview

The dataset contains multiple CSV files representing sales, products, and customer information.

The main goal is to transform the raw data into clean, consistent, and analysis-ready datasets.

### Main Tasks

* Load the Meridian Health CSV files
* Combine the three sales-group files
* Handle renamed and reordered columns
* Standardize quantity and price columns
* Format `sale_date` as `DD/MM/YYYY`
* Clean text-based prices such as `$123.45`
* Normalize doctor names
* Standardize dosage abbreviations
* Split `pack_info` into:

  * Pack Size
  * Strength
  * Form
* Extract promo codes from sales notes
* Join sales data with product `cost_price`
* Calculate:

  * Sales Amount
  * Cost Amount
  * Profit
  * Margin %
* Extract customer loyalty information
* Clean customer names
* Standardize phone numbers
* Remove duplicate customer records

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Regular Expressions (re)**
* **Jupyter Notebook**

## 📂 Project Structure

```text
Meridian-Health-Data-Cleaning/
│
├── Meridian_Health_Data_Cleaning.ipynb
├── cleaned_sales.csv
├── cleaned_customers.csv
├── README.md
│
└── data/
    ├── sales_1.csv
    ├── sales_2.csv
    ├── sales_3.csv
    ├── product_catalog.csv
    ├── customers.csv
    └── other CSV files
```

> The raw dataset files are not included in this repository unless permitted by the dataset owner.

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Meridian-Health-Data-Cleaning.git
```

### 2. Open the project

```bash
cd Meridian-Health-Data-Cleaning
```

### 3. Install the required library

```bash
pip install pandas jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Meridian_Health_Data_Cleaning.ipynb
```

### 5. Add the CSV files

Place the Meridian Health CSV files in the same folder as the notebook, or update the `DATA_FOLDER` path in the notebook.

### 6. Run the notebook

Run the cells from top to bottom.

The notebook will generate:

```text
cleaned_sales.csv
cleaned_customers.csv
```

## 🧹 Data Cleaning Process

### Sales Data

The three sales files are combined into one dataset.

Different column names are standardized, for example:

```text
qty → quantity
amount → unit_price
```

This allows the files to be analyzed consistently.

### Dates

Sales dates are converted to:

```text
DD/MM/YYYY
```

### Prices

Text prices such as:

```text
$123.45
$1,250.00
```

are converted into numeric values.

### Doctor Names

Doctor names are cleaned and standardized to consistent capitalization.

### Dosage

Common dosage variations such as:

```text
milligram
milligrams
mg.
```

are standardized to:

```text
mg
```

Similar transformations are applied to `ml` and `mcg`.

### Pack Information

The `pack_info` field is separated into:

```text
Pack Size
Strength
Form
```

### Promo Codes

Promo codes are extracted from sales notes using pattern matching.

## 💰 Financial Metrics

The cleaned sales data is enriched with product cost information.

### Sales Amount

```text
Sales Amount = Quantity × Unit Price
```

### Cost Amount

```text
Cost Amount = Quantity × Cost Price
```

### Profit

```text
Profit = Sales Amount − Cost Amount
```

### Margin Percentage

```text
Margin % = (Profit ÷ Sales Amount) × 100
```

## 👥 Customer Data Cleaning

Customer records are processed to:

* Extract loyalty status
* Standardize customer names
* Remove unnecessary spaces
* Normalize phone numbers
* Remove exact duplicate records
* Identify duplicate people using cleaned phone numbers

## 📊 Output

The project produces two cleaned datasets:

### `cleaned_sales.csv`

Contains the combined and cleaned sales information, including the calculated financial metrics.

### `cleaned_customers.csv`

Contains cleaned customer information, including standardized names, phone numbers, loyalty status, and duplicate removal.

## 🎯 Learning Objectives

This project demonstrates practical data-analysis skills including:

* Data ingestion
* Data cleaning
* Data standardizatio
