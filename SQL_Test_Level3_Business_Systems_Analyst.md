# 💼 SQL Test – Business Systems Analyst (Level 3)

**Duration:** 60 minutes  
**Instructions:**  
- You may use any SQL dialect (MySQL, PostgreSQL, etc.)  
- Write clean and readable SQL  
- Add comments if needed

---

### 🔹 Question 1: Identify Missing Forecasts

**Scenario:**  
Some active SKUs are missing forecast data for May 2025. You’ve been asked to identify which ones.

**Tables:**
- `forecast_data(sku_id, forecast_month, forecast_qty, location)`
- `sku_master(sku_id, sku_name, status, category)`

**Task:**  
Write a SQL query to find all SKUs that are **active** (`status = 'Active'`) but have **no forecast entry** in May 2025.

**Expected Output Columns:**  
`sku_id`, `sku_name`

---

### 🔹 Question 2: Monthly Forecast KPIs

**Scenario:**  
You need to generate KPI metrics per SKU for May 2025 to help planners make decisions.

**Table:** `forecast_data(sku_id, forecast_month, forecast_qty, location)`

**Task:**  
Write a query that shows for each `sku_id`:  
- Total forecast quantity (`total_forecast_qty`)  
- Number of unique locations (`num_locations`)  
- Average forecast per location (`avg_forecast_per_location`)  

**Expected Output Columns:**  
`sku_id`, `total_forecast_qty`, `num_locations`, `avg_forecast_per_location`

---

### 🔹 Question 3: Delivery Delay Classification

**Scenario:**  
You are analyzing order delays. Orders delayed by more than 7 days are considered critical.

**Tables:**
- `orders(order_id, sku_id, planned_delivery_date, actual_delivery_date)`
- `sku_info(sku_id, sku_name, category)`

**Task:**  
Write a query that shows for each order:
- Days of delay (`delay_days`)
- A flag (`delay_flag`) with:  
  - `'Critical Delay'` if delay > 7 days  
  - `'Minor Delay'` if delay between 1–7 days  
  - `'On Time'` if no delay

**Expected Output Columns:**  
`order_id`, `sku_name`, `category`, `planned_delivery_date`, `actual_delivery_date`, `delay_days`, `delay_flag`
