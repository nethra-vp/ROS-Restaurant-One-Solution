# 📊 ROS Analytics Project

## 🧩 Project Overview

This project delivers end-to-end analytics for **Restaurant One Solution (ROS)** using a visual **KNIME Analytics Platform** workflow (`ROS_final.knwf`). The workflow processes restaurant operational data and visualizes **Key Performance Indicators (KPIs)** to help stakeholders monitor performance, identify bottlenecks, and make data-driven decisions.

The datasets used in this project are **collected and synthetically generated for restaurants operating in the United Kingdom (UK)**, reflecting UK-specific dining patterns, customer behavior, payment preferences, and delivery performance.

---

## 🧰 Platform & Tools

* **Analytics Tool**: [KNIME Analytics Platform](https://www.knime.com/)
* **Workflow File**: `ROS_final.knwf`
* **Workflow Type**: Visual, drag-and-drop data pipeline
* **Outputs**: Tables, charts, and exportable reports

---

## 📈 Key Performance Indicators (KPIs)

### 1. 🏪 Restaurant Performance Metrics

* **Total Revenue by Restaurant**: Sum of `OrderTotal` grouped by `RestaurantID`
* **Average Order Value (AOV)**:

  ```
  AOV = Total Order Amount / Number of Orders
  ```
* **Order Type Distribution**: Dine-In, Takeaway, Home Delivery

### 2. 👥 Order & Customer Insights

* **Peak Order Hours**: Time-based analysis using `OrderDateTime`
* **Customer Retention**: Customers placing multiple orders
* **Order Cancellation Rate**:

  ```
  (Cancelled Orders / Total Orders) × 100
  ```

### 3. 💰 Tax & Revenue Insights

* **Revenue by Tax Type**: Grouped by `TaxApplicable`
* **Convenience Fee Contribution**:

  ```
  (ConvenienceFee / Total Revenue) × 100
  ```

### 4. 🚚 Delivery Partner Metrics

* **Delivery Timeliness Categories**:

  * On-Time: < 30 minutes
  * Slightly Late: 30–45 minutes
  * Delayed: 45–60 minutes
  * Very Late: > 60 minutes

### 5. 💳 Payment Metrics

* **Payment Success Rate**:

  ```
  (Successful Payments / Total Payments) × 100
  ```
* **Payment Mode Distribution**: Card, Cash, UPI
* **Failed Payment Analysis**: Failure trends by `PaymentMode` and `OrderID`

### 6. 📊 General Business Insights

* **Active vs Inactive Restaurants**: Based on `Status`
* **Revenue by Cuisine**: Identification of high-performing cuisines
* **Restaurant Performance Score**:

  * **Performance Ratio** = `Actual Revenue / Expected Revenue`
  * **Rating Bands**:

    * Excellent: ≥ 1.0
    * Good: 0.8 – 0.99
    * Needs Improvement: 0.6 – 0.79
    * Poor: < 0.6

---

## 🚀 How to Open and Run the KNIME Workflow

### Prerequisites

* Install **KNIME Analytics Platform** (version 4.7 or later recommended)
* Java (bundled with KNIME installer)

### Opening the `.knwf` File

You can open the workflow using **any one** of the following methods:

**Method 1: Open via KNIME Menu**

1. Launch **KNIME Analytics Platform**
2. Import the workflow: File → Import KNIME Workflow

**Method 2: Drag and Drop**

1. Open **KNIME Analytics Platform**
2. Drag `ROS_final.knwf` directly into the KNIME workspace

**Method 3: Double-Click (if associated)**

* Double-click `ROS_final.knwf` from your file system (works if KNIME is set as the default application)

### Running the Workflow

1. Configure input data paths if required (CSV or database nodes)
2. Execute the workflow nodes
3. Inspect output tables and visualizations
4. Export results as CSV, Excel, or HTML dashboards 

---

## 📂 Project Structure

```bash
ROS_Analytics_Project/
├── datasets/              # Input datasets (CSV or related files)
├── Project_ROS1.knwf      # KNIME analytics workflow
```

---

## 📌 Notes

* This project is suitable for **academic analysis, portfolio demonstration, and business analytics use cases**
* Data is UK-centric and may need adjustments for other regions
* Workflow nodes are modular and can be extended for additional KPIs

