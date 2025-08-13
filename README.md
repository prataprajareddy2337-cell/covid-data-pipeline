# COVID-19 Data Pipeline using Python & AWS S3

An end-to-end **ETL (Extract, Transform, Load)** pipeline that fetches live COVID-19 data, processes it into a clean format, and stores it in an **AWS S3 bucket** for further analytics or reporting.  
This project demonstrates skills in **data engineering, cloud integration, and automation**.

![COVID Pipeline Architecture](https://github.com/prataprajareddy2337-cell/covid-data-pipeline/blob/main/covid_pipeline_architecture.png)

---

## 📌 Features
- **Automated Data Fetching** – Pulls real-time COVID-19 data from public APIs.
- **Data Transformation** – Cleans and normalizes data using Python and Pandas.
- **Cloud Storage Integration** – Uploads processed datasets to AWS S3 for secure storage.
- **Scalable Pipeline** – Can be extended to handle more data sources or different datasets.
- **Google Colab Friendly** – Runs entirely in Google Colab for easy setup.

---

## 🛠 Tech Stack
- **Python 3**
- **Pandas** for data manipulation
- **Boto3** for AWS S3 integration
- **Requests** for API calls
- **AWS S3** for cloud storage
- **Google Colab** as the development environment

---

## ⚙️ How It Works
1. **Extract**  
   - `fetch_data.py` calls a public COVID-19 API (`disease.sh`) to retrieve the latest global and country-level data.
   - Stores the raw JSON data locally or directly in AWS S3.

2. **Transform**  
   - `transform_data.py` processes the raw data:
     - Normalizes columns
     - Cleans missing values
     - Adds computed metrics

3. **Load**  
   - Uploads the final dataset (CSV/JSON) into an AWS S3 bucket.

---

## 🚀 Getting Started

### **1. Clone the repository**
```bash
git clone https://github.com/prataprajareddy2337-cell/covid-data-pipeline.git
cd covid-data-pipeline
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Set AWS Credentials
Make sure you have your AWS keys stored as environment variables:

bash
Copy
Edit
export AWS_ACCESS_KEY_ID="your_access_key"
export AWS_SECRET_ACCESS_KEY="your_secret_key"
export AWS_SESSION_TOKEN="your_session_token"
export AWS_REGION="your_region"
4. Run the pipeline
bash
Copy
Edit
python scripts/fetch_data.py
python scripts/transform_data.py
📊 Sample Output
Country	Cases	Deaths	Recovered	Date
USA	10234	210	9850	2025-08-12
India	8530	125	8320	2025-08-12

💡 Future Improvements
Automate daily pipeline with AWS Lambda + CloudWatch

Store historical data for trend analysis

Build a dashboard in Power BI or Tableau



👤 Author
Pratap Raja Reddy
📧 Email: your.email@example.com
🔗 LinkedIn | GitHub
