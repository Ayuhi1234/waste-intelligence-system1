# Intern Execution Plan (Sprint 1)

## 🎯 Goal: End-to-End "Hello World"
**Objective:** Get a single piece of sensor data from the backend to the frontend dashboard.

### 👷 Frontend Intern Tasks
* **[Day 1] Repo Setup:** Initialize React with Tailwind CSS. Create the folder structure.
* **[Day 2] Component Library:** Build a static `BinCard` component (showing ID, Fill Level, Status).
* **[Day 3-4] API Integration:** Connect the dashboard to `GET /api/bins`. Handle "Loading" and "Error" states.
* **[Day 5] Polish:** Add a visual indicator for "Critical" bins (Red color if fill > 90%).

### 🤖 ML Intern Tasks
* **[Day 1] Data Mocking:** Write a Python script to generate a CSV with fake sensor data (columns: `bin_id`, `fill_level`, `timestamp`).
* **[Day 2-3] Baseline Model:** Train a simple Logistic Regression model to predict "Pickup Needed (Yes/No)" based on fill level.
* **[Day 4-5] API Wrapper:** Wrap the model in a simple Python script that takes a JSON input and returns a prediction.