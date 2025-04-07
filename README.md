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

| Column | Description |
|--------|-------------|
| `booking_id` | Unique identifier for each booking |
| `hotel` | Type of hotel – Resort or City |
| `lead_time` | Number of days between booking and arrival |
| `arrival_date_year/month/week_number/day` | Arrival dates |
| `stays_in_weekend_nights` | Nights spent over weekends |
| `stays_in_week_nights` | Nights spent on weekdays |
| `adults/children/babies` | Count of each type of guest |
| `meal` | Type of meal package |
| `assigned_room_type` | Final room type assigned |
| `reserved_room_type` | Room type initially booked |
| `booking_changes` | Number of changes made to the booking |
| `market_segment` | Booking origin (e.g., OTA, Direct) |
| `distribution_channel` | How the booking was made |
| `is_repeated_guest` | 1 = Repeated guest, 0 = New guest |
| `previous_cancellations` | Count of past cancellations |
| `deposit_type` | No Deposit / Non-Refund etc. |
| `customer_type` | Transient, Group, etc. |
| `reservation_status` | Final status of the booking |
| `adr` | Average Daily Rate |
| `total_of_special_requests` | Count of guest requests |

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


