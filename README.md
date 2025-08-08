# Flight Delay Prediction System - "Delay Dissatisfaction (D2)" 
## Project Overview
An enterprise-scale machine learning pipeline built to predict flight delays 15+ minutes in advance with 2-3 hours lead time, addressing customer experience and airline operational efficiency challenges.
Authors
UC Berkeley I-School Machine Learning at Scale Final Project (Spring 2024)


Developers and Authors: _Thomas Dolan, Nathan Arias, I-Hsiu Kao, Maegan Kornexl_


## Team 1, Emerald Airlines UI/UX Feature Research Department
### Problem Statement
Business Impact:

7,000-9,000 flights delayed daily (25% of all flights annually)
Costs airlines ~$20,000/hour and passengers ~$47/hour
Significant impact on customer loyalty and brand reputation

Customer Research Findings:

87% of passengers prefer advance delay notification
83% want 2-3 hours advance notice for suspected delays
False positives severely damage customer trust

Technical Architecture
Data Sources & Scale

31.67M flight records from US Department of Transportation
Weather data from NOAA (temperature, pressure, precipitation)
Airport metadata from OurAirports database
Processing: Apache Spark distributed computing framework

Feature Engineering

Temporal Patterns: Federal holiday windows, day-of-week effects, time-of-day analysis
Weather Integration: Multi-dimensional meteorological feature correlation
Domain Features: Airport performance metrics, airline historical data

Model Development
Algorithms Implemented:

Logistic Regression (baseline)
Decision Tree Classification
XGBoost (ensemble methods)
Multilayer Perceptron (neural networks)

Best Performance:

Model: Multilayer Perceptron
Precision: 28.18% (test set)
F-0.5 Score: 31.48% (optimized for minimal false positives)

Evaluation Metrics

F-0.5 Score: Prioritizes precision over recall to minimize false positive notifications
Business-Aligned: Optimized for customer trust while maximizing delay detection
Cross-Validation: Time-series aware validation to prevent data leakage

Key Technical Achievements

Distributed Computing: Processed 31M+ records using Apache Spark
Multi-Source Data Fusion: Integrated aviation, weather, and temporal datasets
Production-Ready Pipeline: End-to-end ML workflow with proper validation
Business Optimization: Custom metrics aligned with customer experience goals

Results & Impact

Successfully identified non-linear patterns in flight delay data
Achieved meaningful precision for early delay prediction
Established framework for real-time deployment
Demonstrated significant improvement over baseline models

Technologies Used

Big Data: Apache Spark, Databricks, Google Cloud DataProc
Machine Learning: scikit-learn, XGBoost, TensorFlow/Keras
Data Processing: pandas, NumPy, PySpark
Languages: Python, SQL

Future Directions

Implementation of early stopping for better generalization
Real-time streaming data integration
Enhanced feature engineering with additional external data sources
Production deployment with monitoring and A/B testing

Project Structure
├── data/                   # Data processing and ETL pipelines
├── notebooks/             # Jupyter notebooks for EDA and modeling
├── src/                   # Source code for models and utilities
├── docs/                  # Project documentation and presentations
└── README.md             # This file
Course Context
This project was completed as the final assignment for DATASCI 261: Machine Learning at Scale at UC Berkeley's School of Information, demonstrating proficiency in distributed computing, large-scale machine learning, and production ML system design.

For questions or collaboration opportunities, please reach out to any of the team members
