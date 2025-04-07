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

1. **Understand the distribution of meal plans (e.g., BB, HB, FB, SC) and identify any patterns or preferences.**

![image](https://github.com/user-attachments/assets/1dd0c3a2-f506-4e53-8911-7e09342be8d9)

- Query-Explanation:
This query analyzes the distribution of meal preferences across all bookings. Here's what each part does:

     * Selects the meal type from the meal_and_stay_details table
     *	Counts the total number of bookings for each meal type
     *	Calculates the percentage share of each meal type
     *	Uses a subquery (SELECT COUNT(*) FROM meal_and_stay_details) to get the total bookings count
     *	Multiplies by 100 and rounds to 2 decimal places for readability
     *	Specifies the source table (meal_and_stay_details)
     *	Groups results by meal type to aggregate the counts
     *	Sorts results by total bookings in descending order (most popular meals first)

- Purpose:
     This query helps understand:
     *	The popularity distribution of different meal options
     *	Which meal types are most/least preferred by guests
     *	The relative market share of each meal category

- Query Result   :
  
 ![image](https://github.com/user-attachments/assets/f2a9e038-4b5b-4d62-888b-7ce8c76d72a7)
 
 ![image](https://github.com/user-attachments/assets/24b0d03d-04dd-44dd-8e79-fb547fab48b0)

 
 

2. **Understand the distribution of bookings across different market segments and calculate summary statistics for lead times within each segment.**

![image](https://github.com/user-attachments/assets/ab47cba1-aa44-4d4d-afd6-91beda3141a6)

 
- Query Explanation:

This SQL query analyzes booking distribution across different market segments. Here's what each part does:

1.	Columns Selected:
-	`b.market_segment_id` (aliased as Market_Segment_ID): The unique identifier for each market segment
-	`m.market_segment` (aliased as Market_Segment_Name): The descriptive name of each market segment
-	`count(b.Booking_id)` (aliased as Bookings): Counts the number of bookings per segment

2.	Tables Used:
-	`booking_source_and_history` (aliased as b): Contains booking records with segment IDs
-	`market_segment` (aliased as m): Contains segment ID-name mappings

3.	 Join Operation:
-	Inner join on `market_segment_id` connects booking records with segment names

4.	 Grouping:
-	Results are grouped by both segment ID and name to ensure accurate counting

- Purpose:
This query provides a clear view of booking volume distribution across different market segments, enabling analysis of which customer segments generate the most business. The results show both the technical ID and human-readable name for each segment along with their respective booking counts.

- Query Result   :

  ![image](https://github.com/user-attachments/assets/80c5e12f-5256-4054-8b57-2109e7ade2ec)


3.  **Analyze the impact of booking changes on cancellation rates. Calculate cancellation rates for bookings with different numbers of changes.**

![image](https://github.com/user-attachments/assets/b3970bc1-abf8-407b-8f64-ceafbea9c7d2)

 
- Query Explanation:
      This query analyzes the relationship between booking modifications and cancellation rates. Here's the breakdown:

  1.	Columns Selected:
  
         * rd.booking_changes: Number of modifications made to each booking
         * COUNT(b.booking_id): Total number of bookings for each modification count
         * SUM(CASE WHEN...Canceled...): Count of canceled bookings per modification count
         * Cancellation rate calculation: Percentage of bookings canceled per modification count
  2.	Tables Joined:
        
          * booking_details (core booking information)
          * room_details (contains booking_changes data)
          * reservation_status (contains cancellation status)
      
    3.	Key Corrections:
  
          * Changed SUN to SUM (function name correction)
          * Fixed the cancellation rate calculation to use canceled status
          * Standardized JOIN syntax

- Purpose:
   This query helps understand:
   •	How frequently bookings are modified
   •	Whether modification frequency correlates with cancellation likelihood
   •	The cancellation risk associated with different numbers of booking changes
   The results can help identify if multiple booking changes serve as an early warning indicator for potential cancellations.

- Query Result   :

![image](https://github.com/user-attachments/assets/280250ee-f2a2-40c5-a585-c1ae06c6653a)


---

## 📊 Sample Power BI Dashboard Questions

1. **Visualize booking trends over the years, including the number of bookings, cancellations, and average lead time. Identify seasonality patterns.**

![image](https://github.com/user-attachments/assets/5eb0f8cd-f20e-4e23-8f9e-588ced6ad063)

   
2. **Compare stays in weekend nights and weekday nights to determine preferences and variations by hotel type.**

![image](https://github.com/user-attachments/assets/7a9f6cb1-d9bb-4f63-a52e-d60f9b6cc54e)

   
3. **Visualize the distribution of reserved and assigned room types. Analyze whether guests tend to receive the room type they initially reserved.**

![image](https://github.com/user-attachments/assets/6d3b0d56-e51b-4c77-89e0-9ae113011ba4)

   

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


