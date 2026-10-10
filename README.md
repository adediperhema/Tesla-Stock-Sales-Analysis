# 🚘 Tesla Stock Sales Analysis 
Power BI + Excel Dashboard Project | 5 Tesla Models | State-wise Sales Insights  

## 📚 Table of Contents  
* [Project Overview](#project-overview)  
* [Tools & Technologies](#tools--technologies)  
* [Excel for Data Formatting & Pre-Processing](#excel-for-data-formatting--pre-processing)  
* [Dataset Breakdown](#dataset-breakdown)  
* [Data Transformation](#data-transformation)  
* [Power BI Dashboard](#power-bi-dashboard)  
* [Insights & Findings](#insights--findings)  
* [Recommendations](#recommendations) 


---

### Project Overview  
This project explores **state-wise stock sales data** for used Tesla vehicles across the U.S., leveraging **Power BI dashboards** to compare model performance, price trends, mileage, and accident history.

The goal is to extract insights into:
- Average pricing  
- Odometer readings  
- Regional market trends  

For the five most common Tesla models:
- Model 3  
- Model Y  
- Model S  
- Model X  
- Cybertruck

---

### Tools & Technologies  
- Microsoft Power BI (for dashboard creation)  
- Excel (data formatting & pre-processing)  
- Power Query (ETL in Power BI)  
- DAX (measures and KPIs)  


---

### Excel for Data Formatting & Pre-Processing  

- Cleaned missing values and duplicates  
- Formatted numeric fields (e.g., price, mileage, EMI)  
- Standardized column names and categories  
- Created calculated fields. 

> Excel was used for quick and efficient pre-processing before loading data into Power BI.

<img width="1387" height="607" alt="Tesla Sales Table Image 1" src="https://github.com/user-attachments/assets/d2fa12e9-7ac2-4da8-a0c0-99e03f1ae346" />



### Dataset Breakdown  
The dataset used for this analysis includes:
- Tesla model name  
- Average price (USD)  
- Median odometer (miles)  
- EMI (Estimated Monthly Installment)  
- State of sale  
- Accident history (% with or without)  
- Driver Assist System type:
  - Full Self-Driving (FSD)  
  - Enhanced Autopilot  
  - Standard Autopilot  

Each vehicle record was filtered and grouped to compute KPIs across states.

---

### Data Transformation  
Using **Power Query** and **DAX**, the data was transformed to calculate:  
- Average price per model/state
```
Average Price = AVERAGE('Tesla Stock Dataset'[price])
```

- Median mileage (odometer)
```
Median Odometer = MEDIAN('Tesla Stock Dataset'[odometer])
```

- EMI estimates
```
Average_EMI = AVERAGE('Tesla Stock Dataset'[EMI])

```

- Accident percentage
```
PercentWithAccident = [With Accident]/ SUM('Tesla Stock Dataset'[accident_history] * 100
```

- Percent With No Accident
```
PercentNoAccident = [Without Accident]/ SUM('Tesla Stock Dataset'[accident_history] * 100
``` 

Visuals were color-coded by driver assist systems and filtered by model.

---

### Power BI Dashboard  
Each Tesla model has a dedicated dashboard featuring the following key visuals:
- Average Price  
- Median Odometer  
- EMI  
- % With/Without Accident  
- Price by State  
- Mileage by State  
- Average Price by Driver Assist System (DAS)  
- 3D Vehicle View (UI/UX enhancement)

<img width="1247" height="737" alt="Tesla Sales Image 2" src="https://github.com/user-attachments/assets/88be3677-d477-4e37-84d0-864442a7ec7e" />


<img width="1247" height="737" alt="Tesla Sales Image 3" src="https://github.com/user-attachments/assets/023327cb-e454-488d-8599-e9556f857510" />


<img width="1247" height="736" alt="Tesla Sales Image 4" src="https://github.com/user-attachments/assets/008ac1f6-46fb-477b-a4d6-8788e479cfcf" />


<img width="1251" height="735" alt="Tesla Sales Image 5" src="https://github.com/user-attachments/assets/4b2890ac-4e7c-405f-8466-7c9cb4dbc7c5" />


<img width="1250" height="737" alt="Tesla Sales Image 6" src="https://github.com/user-attachments/assets/d7dd8f36-d376-4bfa-b97a-9ebc662fab04" />



---

### Insights & Findings  
1. **Model Y** is the most affordable option at ~$33.9K with the lowest EMI ($529.37).  
2. **Model X** has the highest average price and EMI, making it the most premium used Tesla option.  
3. **Model 3** is the most balanced in terms of price vs. mileage.  
4. **Cybertruck** data suggests it's new to the market (lower mileage) but priced mid-range.  
5. **States like NY, OH, NC, VA** appear across the top for mileage, suggesting high usage or resales.  
6. **Accident-free rate** is high across all models, with **Model 3 and Y** being the safest (>90%).

---

### Recommendations  

#### 1. 🎯 Target High-Volume States  
Focus marketing and resale efforts in states like **NY, OH, NC, VA**, which show high vehicle turnover and mileage demand.

#### 2. 💼 Price Based on DAS  
Use **Driver Assist System tiers** as a pricing lever.  
> Full Self-Driving variants command significantly higher average prices (up to **$63.2K**).

#### 3. 📉 Promote Lower EMI Models  
**Model Y and Model 3** with lower EMIs may be ideal for entry-level EV buyers or fleet purchases.

#### 4. 🔍 Expand Dataset for Model Y & Cybertruck  
As newer models, their datasets will grow. Monitoring pricing trends can help forecast **depreciation** and **resale value**.

---

