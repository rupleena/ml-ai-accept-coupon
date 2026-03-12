# 🚗 Coupon Acceptance Analysis  
## Practical Application

---

# 1. Project Overview (Non-Technical Summary)

This project analyzes customer behavior when drivers receive digital coupons while traveling. The goal is to understand what factors influence whether a driver **accepts or rejects a coupon**.

The dataset contains simulated driving scenarios in which drivers receive coupons for nearby businesses such as **coffee houses, bars, and restaurants**. Each record includes information about the driver, the driving situation, and the type of coupon offered.

Using data analysis and visualization techniques, patterns were identified to highlight the differences between customers who accepted coupons and those who rejected them.

Understanding these behavioral patterns can help businesses design **better targeted promotional campaigns** and increase coupon redemption rates.

## Key Features Considered

The following features were taken into account during the analysis to understand the factors influencing coupon acceptance:

- **Driver Demographics:**  
  Age, gender, marital status, and education level of the driver.

- **Travel Context:**  
  Whether the driver was alone, with friends, or with children; direction of travel; timing of the trip.

- **Coupon Attributes:**  
  Type of coupon (e.g., bar, coffee house, carry-out, restaurant); time when coupon was presented.

- **Lifestyle and Behavioral Patterns:**  
  Frequency of visits to similar businesses (e.g., how often the driver frequents bars or coffee houses).

- **Situational Factors:**  
  Distance to the location offering the coupon, weather conditions, and whether the coupon matches the current activity.

These features were selected based on their potential impact on the decision-making process regarding coupon acceptance.


---

# 2. Key Differences Between Customers Who Accepted and Rejected Coupons

The analysis revealed several noticeable differences between drivers who accepted coupons and those who rejected them.

## Customers Who Accepted Coupons

Drivers were more likely to accept coupons when:

- They **frequently visited the same type of business** as the coupon being offered.
- They were **younger drivers**, particularly under the age of 30.
- They were **traveling alone or with friends** rather than with children.
- The coupon matched their **existing lifestyle habits**, such as regularly visiting coffee houses or bars.
- The timing of the coupon aligned with typical behavior (for example, coffee coupons in the morning).

## Customers Who Rejected Coupons

Drivers were less likely to accept coupons when:

- They **rarely visit the type of business** being promoted.
- They were **traveling with children**, which may limit flexibility to stop.
- The coupon did not match their **typical consumer habits**.
- The promotion appeared during a time when the driver was **less likely to visit that type of establishment**.

---

# 3. Insights From Specific Coupon Types

## 🍺 Bar Coupons

Several behavioral patterns were observed for bar coupons.

Drivers who visited bars **more than once per month** were significantly more likely to accept bar coupons compared to those who rarely visited bars.

Passenger type also influenced acceptance rates. Drivers traveling **without children** were more likely to accept bar coupons.

### Time of Use for Bar Coupons

Bar coupons were most effective during **late afternoon and evening hours**, particularly around **6 PM and 10 PM**. These times align with typical social or leisure activities when drivers may be more likely to visit bars.

Bar coupons were **less likely to be accepted in the morning**, which suggests that timing plays a key role in promotion effectiveness.

## ☕ Coffee House Coupons

Drivers who frequently visit coffee houses were more likely to accept coffee coupons.

Acceptance was also higher during **morning hours**, when drivers are likely commuting to work or starting their day.

Drivers traveling **alone or with friends** were more likely to accept coffee coupons compared to drivers traveling with children.

---

# 4. Business Recommendations

Based on the analysis, businesses using mobile coupon marketing can improve redemption rates by targeting specific customer segments.

Recommended strategies include:

- Target customers who **already visit similar establishments frequently**
- Send **coffee coupons during morning commuting hours**
- Send **bar coupons during late afternoon or evening hours**
- Target **younger drivers**, who show higher coupon engagement
- Avoid sending **bar coupons to drivers traveling with children**

These strategies can help businesses deliver more relevant promotions and improve marketing effectiveness.

---

# 5. Technical Report

## Dataset

The dataset contains **12,684 records** representing simulated driving scenarios where drivers receive coupons for nearby businesses.

Each record includes:

### User Attributes
- Gender
- Age
- Marital status
- Number of children
- Education
- Occupation
- Income
- Frequency of visiting bars, coffee houses, and restaurants

### Contextual Attributes
- Driving destination
- Passenger type
- Weather
- Temperature
- Time of day
- Direction relative to destination

### Coupon Attributes
- Coupon type
- Coupon expiration time

### Target Variable

`Y`

- **1 = Coupon accepted**
- **0 = Coupon rejected**

---

## Data Cleaning

The following preprocessing steps were performed:

### Handling Missing Data

The **car** column contained more than 99% missing values and was removed from the dataset.

Other columns contained small numbers of missing values. Since these represented less than 5% of the total dataset, rows containing missing values were removed.

### Removing Duplicates

A total of **74 duplicate records** were identified and removed.

### Final Dataset Size

| Stage | Records |
|------|------|
| Original Dataset | 12,684 |
| After Removing Duplicates | 12,610 |
| After Removing Missing Values | 12,007 |

---

## Exploratory Data Analysis

Exploratory data analysis was performed using **Pandas**, **Matplotlib**, and **Seaborn** to understand the dataset structure and identify patterns in coupon acceptance.

### Descriptive Statistics

Statistical summaries were generated to understand distributions of variables such as:

- Temperature
- Presence of children
- Distance to coupon location
- Direction of travel

### Data Investigation

The dataset was inspected for:

- Missing values
- Duplicate records
- Data type consistency
- Unique categorical values

---

## Visualization

Several visualizations were created to analyze coupon acceptance patterns.

Examples include:

- Coupon acceptance rates by **coupon type**
- Acceptance rates based on **frequency of visiting bars**
- Comparison of **driver demographic groups**
- Acceptance rates under specific behavioral conditions

Visualization libraries used:

- **Matplotlib**
- **Seaborn**

---

# 6. Repository Structure

This repository is organized as follows:


├── data/         # Contains datasets used for analysis
├── images/       # Stores generated figures and visualizations
├── prompt.ipynb  # Jupyter Notebook with code, analysis, and results
└── README.md     # Project overview and documentation


---

# 7. Tools Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 8. Conclusion

This project demonstrates how exploratory data analysis and visualization can help uncover behavioral patterns in consumer decision making.

The results suggest that **lifestyle habits, passenger context, age, and timing** all influence whether drivers accept location-based coupons.

Businesses can use these insights to deliver **more personalized and timely promotions**, increasing the likelihood that customers will redeem coupons.