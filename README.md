# 🚀 FraudStream Data Platform

## 📌 Project Overview

FraudStream is a real-time fraud detection data platform built using AWS, Databricks, and PySpark Structured Streaming.

The platform ingests live financial transaction data, processes it using streaming ETL pipelines, applies fraud detection logic using window-based and stateful processing, and stores results in a Delta Lakehouse using Medallion architecture (Bronze, Silver, Gold).

This project demonstrates modern Data Engineering concepts including cloud-native streaming, fault-tolerant processing, and scalable data lake design.

---

## 🏗️ Architecture
Transaction Generator (Python)
↓
AWS Kinesis Data Stream
↓
Databricks Structured Streaming
↓
Bronze Layer (Raw Delta)
↓
Silver Layer (Cleaned & Enriched)
↓
Fraud Rules Engine
↓
Gold Layer (Fraud Alerts & KPIs)
↓
SQL Analytics / Dashboard


---

## 🛠️ Tech Stack

- Amazon Web Services (AWS)
  - Kinesis Data Streams
  - S3 (Data Lake Storage)
- Databricks (AWS Version)
- PySpark Structured Streaming
- Delta Lake
- Git & GitHub

---

## 📂 Project Structure
fraudstream-data-platform/
│
├── producer/
│ └── transaction_generator.py
│
├── streaming/
│ ├── 01_bronze_layer.py
│ ├── 02_silver_layer.py
│ ├── 03_fraud_rules_engine.py
│ └── 04_gold_layer.py
│
├── config/
│ └── config.py
│
├── docs/
│ └── architecture.md
│
├── requirements.txt
├── .gitignore
└── README.md


---

## 🔥 Key Features

- Real-time transaction ingestion
- Streaming ETL using PySpark Structured Streaming
- Medallion architecture (Bronze, Silver, Gold)
- Window-based fraud detection
- Stateful aggregations
- Watermarking for late data handling
- Checkpointing for fault tolerance
- Exactly-once processing using Delta Lake
- Cloud-native architecture on AWS

---

## 🥉 Bronze Layer

- Stores raw streaming transaction data
- Append-only Delta table
- Maintains original schema
- Enables replay and auditing

---

## 🥈 Silver Layer

- Cleans and validates transactions
- Filters invalid records
- Adds event timestamp column
- Prepares data for fraud detection logic

---

## 🥇 Gold Layer

- Applies fraud detection rules
- Generates fraud alerts
- Stores aggregated KPIs
- Supports real-time analytical queries

---

## 🚨 Fraud Detection Logic

The system detects suspicious transactions using:

1. High-value transaction rule  
   - Flag if transaction amount > threshold  

2. Velocity rule  
   - More than N transactions from same user within 1 minute  

3. Location anomaly  
   - Same user transacting from different cities in short duration  

4. Statistical anomaly detection  
   - Z-score based outlier detection  

---

## 📊 Data Engineering Concepts Demonstrated

- Structured Streaming (Micro-batch processing)
- Stateful stream processing
- Window-based aggregations
- Watermarking
- Delta Lake ACID guarantees
- Checkpointing and fault tolerance
- Cloud data lake architecture
- Real-time pipeline design

---

## 🎯 Use Case

Financial institutions can use FraudStream to:

- Detect suspicious transactions in real time
- Reduce fraud losses
- Enable faster incident response
- Improve transaction monitoring systems

---

## 🚀 Future Enhancements

- Add real-time dashboard visualization
- Integrate alert notification system (SNS / Email)
- Add ML-based fraud scoring model
- CI/CD pipeline using GitHub Actions
- Infrastructure as Code (Terraform)

---

## 👩‍💻 Author

Renusri Jadala  
Final Year B.Tech CSE  
Data Engineering Enthusiast

---









