# Airline Performance Dashboard - Power BI

![Power BI Logo](https://img.icons8.com/color/48/power-bi.png) 

Welcome to the **Airline Performance Dashboard**! This Power BI project provides a comprehensive analysis of airline flight data, offering insights into key performance metrics such as on-time arrivals, delays, cancellations, and diversions. The dashboard is designed to be interactive, user-friendly, and visually appealing, making it a powerful tool for airline analysts, managers, and enthusiasts.

---

## 🚀 Features

### **Key Metrics**
- **Total Flights**: Total number of flights operated.
- **On-Time Flights**: Number of flights that arrived on time.
- **Delayed, Cancelled, and Diverted Flights**: Breakdown of flight disruptions.
- **On-Time Percentage**: Percentage of flights that arrived on time.

### **Visualizations**
- **Donut Chart**: Percentage of flights operated by each carrier.
- **Bar Chart**: Breakdown of delays, cancellations, and diversions.
- **Map Visual**: Flight routes and airports with the most delays.
- **Tables**: Detailed data for carriers, routes, and time periods.

### **Interactivity**
- **Bookmarks**: Toggle between different views (e.g., overall performance, detailed analysis).
- **Filters**: Filter data by carrier, route, and time period.
- **Buttons**: Reset the dashboard or show/hide additional insights.

---

## 📊 Dataset

The dataset used in this project includes the following columns:
- `Carrier`: Airline carrier name.
- `ArrDelay`: Arrival delay in minutes.
- `Cancelled`: Indicates if the flight was cancelled (`1` = cancelled, `0` = not cancelled).
- `Diverted`: Indicates if the flight was diverted (`1` = diverted, `0` = not diverted).
- `Flights`: Number of flights operated.

---

## 📈 DAX Measures

The following DAX measures were created for analysis:

1. **On-Time Flights**:
   ```DAX
   On-Time Flights = 
   COUNTROWS(
       FILTER(
           DelayedFlights,
           DelayedFlights[ArrDelay] = 0 && DelayedFlights[Cancelled] = 0 && DelayedFlights[Diverted] = 0
       )
   )
![Alt Text](https://github.com/usamasayed/Airline-Power-Bi-Project/blob/main/Screenshots/WhatsApp%20Image%202025-02-06%20at%2023.43.02_48992eb2.jpg)
   
![WhatsApp Image 2025-02-06 at 23 43 25_3c19e30b](https://github.com/user-attachments/assets/fd3600ca-c183-4f1e-a6fc-db57048c7aa6)
