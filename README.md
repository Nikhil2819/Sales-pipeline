# 🛠️ Retail ETL Pipeline (AWS → Snowflake → Dashboard)

## 📌 Project Overview

A fully automated, cloud-native ETL pipeline that processes retail sales data from raw CSV files to interactive analytics dashboards. This project demonstrates modern data engineering practices using AWS services and Snowflake for scalable data processing and visualization.

**🎯 Achievement:** Successfully built an end-to-end automated data pipeline that transforms dirty sales data into actionable business insights.

---

## 🏗️ Architecture

![ETL Pipeline Architecture](diagrams/etl_pipeline.png)

**Data Flow:**
```
Raw CSV Upload → AWS S3 (/raw/) → Lambda ETL Processing → S3 (/cleaned/) → 
Snowflake Data Warehouse → Interactive Snowsight Dashboard
```

---

## ✨ Key Features

- **🔄 Event-Driven Processing**: S3 upload automatically triggers Lambda ETL
- **🧹 Advanced Data Cleaning**: Deduplication, validation, and standardization
- **📊 Real-time Analytics**: Interactive dashboard with 5 visualization types
- **☁️ Serverless Architecture**: Cost-effective, scalable AWS Lambda processing
- **📈 Business Intelligence**: Sales trends, regional performance, product analysis

---

## 🎯 What We Built

### **ETL Processing Engine**
- **Lambda Function**: Python ETL logic with pandas for data transformation
- **Data Cleaning**: Handles duplicates, missing values, format inconsistencies
- **S3 Integration**: Seamless processing between raw and cleaned buckets

### **Data Warehouse & Analytics**
- **Snowflake Setup**: Complete warehouse, database, and schema configuration
- **External Stages**: S3-Snowflake integration for automated data loading
- **Interactive Dashboard**: 5-chart analytics dashboard in Snowsight

### **Sample Data & Testing**
- **Dirty Data Generator**: Custom Python script creates realistic messy datasets
- **150+ Records**: E-commerce transactions across multiple regions and categories

---

## 📸 Project Screenshots

| Component | Screenshot | Description |
|-----------|------------|-------------|
| **S3 Structure** | ![S3](diagrams/s3_structure.png) | Raw & cleaned data organization |
| **Lambda Function** | ![Lambda](diagrams/lambda_code.png) | ETL processing code |
| **Analytics Dashboard** | ![Dashboard](diagrams/dashboard.png) | Complete 5-chart dashboard |
| **Data Transformation** | ![Before/After](diagrams/before_after_s3.png) | Raw vs cleaned data |

---


## 📁 Project Structure

```
etl-project/
├── data/                          # Sample datasets
│   ├── sample_sales_dirty.csv     # Raw test data (150+ records)
│   └── sample_sales_dirty_cleaned.csv  # Processed data
├── diagrams/                          # Project Screenshots
│   ├── s3_structure.png
│   ├── lambda_code.png
│   ├── dashboard.png
│   └── before_after_s3.png
├── scripts/
│   ├── generate_dirty_data.py     # Data generator for testing
│   └── lambda/
│       └── lambda_function.py     # AWS Lambda ETL code
├── diagrams/
│   └── etl_pipeline.png          # Architecture diagram
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

---


---

## 🚀 Future Enhancements

- [ ] Data quality monitoring alerts
- [ ] Incremental loading strategies
- [ ] Advanced analytics (ML predictions)
- [ ] Mobile-responsive dashboards
- [ ] Automated testing framework
