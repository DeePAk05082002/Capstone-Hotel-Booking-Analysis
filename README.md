# 🏨 Hotel Booking Analysis Project

## 📌 Problem Statement

The objective of this project is to analyze hotel booking data to uncover patterns, guest preferences, and factors influencing booking cancellations. The goal is to use SQL and Excel for data cleaning and exploratory data analysis (EDA), followed by developing a Power BI dashboard to track booking trends and optimize hotel operations.

---

## 📂 Dataset Description

This dataset contains comprehensive details related to hotel bookings including:

- Guest demographics and preferences
- Booking channels
- Meal plans
- Reservation status
- Room types
- Special requests

📊 **Source**: [Hotel Booking Dataset - GitHub (AccioJob)](https://github.com/acciojob-data-analytics/hotel_booking)

---
## 🎥 Video Walkthrough

Check out the full video explanation of this project below:



---

## 🗂️ Table Descriptions

### 1. `Booking_Details`
Core table containing:
- Booking ID
- Hotel type (City / Resort)
- Lead time
- Arrival details (year, month, week, day)
- Weekend and weekday stays
- Cancellation status (0 = Not Canceled, 1 = Canceled)
 
### 2. `Guest_Info`
Details on number of adults, children, and babies per booking.

### 3. `Room_Details`
Captures:
- Reserved room type vs. assigned room type
- Number of room changes

### 4. `Meal_And_Stay_Details`
Includes:
- Meal type
- ADR (Average Daily Rate)
- Parking space requirements
- Special requests count

### 5. `Reservation_Status`
Tracks:
- Final status (Canceled, Check-Out, etc.)
- Date of status change

### 6. `Booking_Source_and_History`
Provides insights on:
- Booking source/channel
- Repeated guests
- Past cancellations and bookings
- Deposit type, customer type, agent/company ID
- Days on waiting list

---

## 🧾 Data Dictionary

### 1. Booking_Details
| Column | Data Type | Description | Possible Values |
|--------|-----------|-------------|-----------------|
| hotel | TEXT | Type of hotel booked | 'Resort Hotel', 'City Hotel' |
| is_canceled | BIGINT | Booking cancellation status | 0 (No), 1 (Yes) |
| lead_time | BIGINT | Days between booking and arrival | 0–737 |
| arrival_date_year | BIGINT | Year of arrival | 2015–2017 |
| arrival_date_month | TEXT | Month of arrival | Jan–Dec |
| arrival_date_week_number | BIGINT | Week number | 1–53 |
| arrival_date_day_of_month | BIGINT | Day of month | 1–31 |
| stays_in_weekend_nights | BIGINT | Weekend nights stayed | 0–19 |
| stays_in_week_nights | BIGINT | Week nights stayed | 0–50 |
| country | TEXT | Guest's country code | ISO code |
| Booking_id | TEXT | Unique booking identifier | Alphanumeric |

### Sample Data
![image](https://github.com/user-attachments/assets/edfb0188-9de6-4616-bdc9-d41dbba15f2a)

### 2. Guest_Info
| Column | Data Type | Description |
|--------|-----------|-------------|
| adults | INT | Number of adults |
| children | INT | Number of children |
| babies | INT | Number of babies |
| Booking_id | TEXT | Foreign key to booking |

### Sample Data
![image](https://github.com/user-attachments/assets/7b35b17c-b909-4916-964c-afe139e94e8e)

### 3. Booking_Source_History
| Column | Data Type | Description |
|--------|-----------|-------------|
| country | TEXT | Guest’s country code |
| market_segment_id | INT | Market segment ID |
| distribution_channel_id | INT | Distribution channel ID |
| is_repeated_guest | INT | 0 = No, 1 = Yes |
| previous_cancellations | INT | Prior cancellations |
| previous_bookings_not_canceled | INT | Past successful bookings |
| deposit_type | TEXT | 'No Deposit', 'Non Refund', 'Refundable' |
| agent | INT | Booking agent ID |
| company | INT | Company ID |
| days_in_waiting_list | INT | Waiting list days |
| customer_type | TEXT | 'Transient', 'Contract', 'Group', 'Transient-Party' |
| Booking_id | TEXT | Foreign key to booking |

### Sample Data
![image](https://github.com/user-attachments/assets/7378d5bc-950e-424f-af72-6014ba87dc28)


### 4. Meal_And_Stay_Details
| Column | Data Type | Description |
|--------|-----------|-------------|
| meal | TEXT | 'BB', 'HB', 'FB', 'SC' |
| adr | DECIMAL | Average Daily Rate |
| required_car_parking_spaces | INT | Number of parking spots |
| total_of_special_requests | INT | Guest special requests count |
| Booking_id | TEXT | Foreign key to booking |

### Sample Data
![image](https://github.com/user-attachments/assets/c36ed0d4-c7bc-4c8f-a955-7b3be12c24cc)


### 5. Reservation_Status
| Column | Data Type | Description |
|--------|-----------|-------------|
| reservation_status | TEXT | 'Check-Out', 'Canceled', 'No-Show' |
| reservation_status_date | DATE | Status update date |
| Booking_id | TEXT | Foreign key to booking |

### Sample Data
![image](https://github.com/user-attachments/assets/32b4197e-0d72-4522-b138-d02a2d6d5804)


### 6. Country
| Column | Data Type | Description |
|--------|-----------|-------------|
| country_code | TEXT | ISO country code |
| country_name | TEXT | Full country name |

### Sample Data          
![image](https://github.com/user-attachments/assets/c27ae26b-0b97-4881-9d83-db164b598f30)


### 7. Room_Details
| Column | Data Type | Description |
|--------|-----------|-------------|
| reserved_room_type | TEXT | Room type booked |
| assigned_room_type | TEXT | Room type assigned |
| booking_changes | INT | Number of modifications |
| Booking_id | TEXT | Foreign key to booking |

### Sample Data
![image](https://github.com/user-attachments/assets/e71473fb-011a-4e05-86a6-db134a61c3cf)


### 8. Distribution_Channel
| Column | Data Type | Description |
|--------|-----------|-------------|
| distribution_channel_id | INT | Unique channel ID |
| distribution_channel | TEXT | 'Direct', 'Corporate', 'TA/TO', 'GDS', etc. |

### Sample Data
![image](https://github.com/user-attachments/assets/82067c28-2862-476f-86d6-a7c6bcec6de9)


### 9. Market_Segment
| Column | Data Type | Description |
|--------|-----------|-------------|
| market_segment_id | INT | Unique segment ID |
| market_segment | TEXT | 'Direct', 'Corporate', 'Online TA', etc. |

### Sample Data
![image](https://github.com/user-attachments/assets/5a491e39-751a-4a08-82c0-aa645acedc6a)



---
## ER Diagram 
 ![image](https://github.com/user-attachments/assets/7684a0ab-1c07-4042-a829-a98f5765d41e)

---

## 🔍 Sample EDA Questions

1. **What is the cancellation rate for each hotel type?**
2. **Which meal plans are most preferred by repeated guests?**
3. **Is there any seasonality in booking trends across months or weeks?**

---

## 📊 Sample Power BI Dashboard Questions

1. **What are the top booking channels and their impact on cancellations?**
2. **How does lead time affect cancellation probability across hotels?**
3. **What trends can be observed in average daily rate (ADR) over time?**

---

## 🛠 Tools Used

- **SQL**: Data extraction and transformation
- **Excel**: Initial data cleaning, pivot tables
- **Power BI**: Data modeling and dashboarding

---

## 📈 Output

An interactive Power BI Reports displaying:
- Booking Trends & Seasonality Report
    ![image](https://github.com/user-attachments/assets/db17d6c5-b99d-4c84-b160-04001976f1c5)

- Guest Demographics & Behavior Report
   ![image](https://github.com/user-attachments/assets/c767d1c5-3bbc-43e8-a8da-04a781c1c130)

- Pricing & Revenue Optimization Report
   ![image](https://github.com/user-attachments/assets/3a659e0f-2310-47a9-8d15-a8228bf55a23)

- Reservation Status & Cancellations Report
   ![image](https://github.com/user-attachments/assets/429dbdb2-6650-4573-89ae-5cc6a13ef7a1)

- Booking Channels & Market Segmentation Report
   ![image](https://github.com/user-attachments/assets/ed38e6c1-5e91-4e01-92a7-92c941fdede1)



---

## 📄 Project Report

Refer to the detailed project report attached in the repo: `Hotel Booking Analysis.pdf`

---

## 🙌 Acknowledgements

Dataset credit: [AccioJob Data Analytics GitHub](https://github.com/acciojob-data-analytics/hotel_booking)

---

## 🚀 Author

**Deepak Chaudhary**  
Data Analyst | Python, SQL, Power BI Enthusiast  
[LinkedIn](www.linkedin.com/in/deepakchaudhary050802) | [GitHub](https://github.com/DeePAk05082002)

---


