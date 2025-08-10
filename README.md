# Metro Capacity Planning

## Project Objective

The goal of this project is to develop a predictive model that optimizes train services by analyzing passenger data during the COVID-19 pandemic.  
In this project, we explore how travel patterns have changed over time and how various factors impact train capacity planning.  
This is a real-world project that was previously implemented for the city of Toronto, Canada.

---

## Project Structure

```
metro-capacity-planning/
├── data/                # Contains the CSV data file
├── notebooks/           # Contains Jupyter notebooks for preprocessing and modeling
│   ├── PPQ1.ipynb       # Preprocessing for Problem 1
│   ├── PPQ2.ipynb       # Preprocessing for Problem 2
│   ├── PPQ3.ipynb       # Preprocessing for Problem 3
│   ├── Q1.ipynb         # Modeling for Problem 1
│   ├── Q2.ipynb         # Modeling for Problem 2
│   └── Q3.ipynb         # Modeling for Problem 3
├── requirements.txt     # List of required libraries for the project
└── README.md            # Project description and instructions
```

---

## Dataset Description

The data is stored in a CSV file inside the `data/` folder, and it contains the following columns:

- **Year**  
- **Month**  
- **Day**  
- **Week Number**: Indicates which week of the year it is  
- **Corridor**: Some stations are junctions for multiple routes  
- **Station**: The station number  
- **Workday**: Whether the day is a working day or not  
- **Period**: Time of the day (Morning, Noon, Afternoon, Night)  
- **Covid19**: Whether there was a COVID-19 alert in that station's region during that time  
- **Ridership**: The number of passengers who boarded the trains on that date  
- **N_trains**: The number of trains that passengers boarded during that time period. (The number of trains is not always accurate, as sometimes the number of passengers exceeds the capacity, and sometimes the number of trains exceeds the required number.)

---

## Problems Addressed

In this project, three different problems were modeled and solved:

### 🔹 Problem 1:
Predicting the number of passengers using only the data from the same day (without using past day information)  
Objective: Build a general model to predict the number of passengers for a specific time period

### 🔹 Problem 2:
Predicting the number of passengers for different time periods **for the next week** using past data  
Objective: Better allocate train capacity for the upcoming week using historical data

### 🔹 Problem 3:
Predicting the number of passengers for different time periods **for the next day** using past data  
Objective: More precise planning for the next day

*In all problems, the "Year" and "Number of Trains" columns were not used.*

---

## Dependencies

The required libraries are listed in the `requirements.txt` file. To install them, use the following command:

```bash
pip install -r requirements.txt
```

---
