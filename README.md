# 🚗 vehicle-co2-consumption-analysis

## 📌 Overview
This project performs an Exploratory Data Analysis (EDA) on vehicle fuel consumption and its relationship with CO₂ emissions. The goal is to standardize units, clean the data, and generate meaningful insights about fuel efficiency and environmental impact.

---

## 📊 Dataset Description
The dataset contains detailed information about vehicles, including engine specifications, fuel type, transmission, fuel consumption, and CO₂ emissions.

- Fuel consumption originally measured in **mpg (miles per gallon)**  
- CO₂ emissions measured in **g/mile (grams per mile)**  
- A unit conversion was applied to ensure consistency between variables  

---

## 🔄 Data Processing & Feature Engineering
Key preprocessing steps include:

- Handling missing values  
- Data type optimization (`category`, `float`, `int`)  

### Created variables:
- `consumo_litros_milla` → conversion from mpg to L/mile  
- `galones_por_milla` → inverse of mpg  

### Feature grouping:
- Transmission type (Manual / Automatic)  
- Drivetrain categories  
- Fuel type classification  
- Engine type grouping  
- Consumption and CO₂ level categorization  

---

## 📊 Data Dictionary

### 🔹 Original Variables

| Column | Type | Description |
|--------|------|-------------|
| Fabricante | object | Vehicle manufacturer |
| modelo | object | Vehicle model |
| year | int64 | Model year |
| desplazamiento | float64 | Engine displacement (liters) |
| cilindros | float64 | Number of cylinders |
| traccion | object | Drivetrain description |
| transmision | object | Transmission description |
| clase | object | Vehicle class |
| combustible | object | Fuel type |
| consumo | int64 | Fuel consumption (mpg) |
| co2 | float64 | CO₂ emissions (g/mile) |

---

### 🔹 Engineered Features

| Column | Type | Description |
|--------|------|-------------|
| Clase_Tipo | category | Vehicle class grouping |
| traccion_tipo | category | Simplified drivetrain |
| transmision_tipo | object | Manual or Automatic |
| combustible_tipo | category | Grouped fuel type |
| tipos_de_motor | category | Engine classification |
| tipos_de_consumo | category | Consumption levels |
| tipos_de_co2 | category | CO₂ emission levels |

---

### 🔹 Derived Variables

| Column | Type | Description |
|--------|------|-------------|
| consumo_litros_milla | float64 | Fuel consumption in L/mile |
| galones_por_milla | float64 | Fuel consumption in gallons per mile |

---

## 🔍 Exploratory Data Analysis (EDA)
The analysis focuses on:

- Distribution of fuel consumption  
- Relationship between fuel consumption and CO₂ emissions  
- Patterns across vehicle types and engine configurations  

---

## 📈 Key Insights
- There is a **positive correlation** between fuel consumption and CO₂ emissions  
- Higher fuel consumption → higher CO₂ emissions  
- Lower fuel consumption → lower CO₂ emissions  

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Google Colab  

---



