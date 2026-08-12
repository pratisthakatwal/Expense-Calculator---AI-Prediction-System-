# 💰 Money Mentor – AI Expense Tracking Android Application

**Money Mentor** is an AI-powered personal expense tracking Android application developed as a final-year dissertation project for the **BSc Computing (Network Engineering)** degree at the **University of Northampton – NAMI College**.

The application helps users manage their personal finances by automatically detecting transactions from bank SMS messages, recording and analysing expenses, visualising spending patterns, managing monthly budgets, and predicting future expenses using machine learning.

---

## 📌 Project Overview

Managing personal finances manually can be time-consuming and makes it difficult to identify spending patterns. Money Mentor addresses this problem by combining **mobile application development, cloud computing, data analytics, and machine learning** into a single expense management system.

The application provides automated expense tracking alongside manual entry, allowing users to monitor their financial activity through interactive dashboards and reports.

### 🎯 Project Objectives

- Automate expense tracking using bank SMS messages
- Provide secure user authentication
- Store expense information in the cloud
- Categorise and analyse personal expenses
- Visualise spending patterns through charts and statistics
- Allow users to set and monitor monthly budgets
- Predict future expenses using machine learning
- Provide downloadable financial reports
- Offer a user-friendly Android interface with dark mode support

---

## ✨ Features

### 🔐 User Authentication
- Firebase Authentication
- Secure user login and registration
- User profile management
- Profile image upload

### 📱 Expense Management
- Automatic bank SMS transaction detection
- SMS transaction parsing
- Manual expense entry
- Expense category selection
- Expense history and tracking

### 📊 Dashboard & Analytics
- Interactive expense dashboard
- Spending statistics
- Category-based expense analysis
- Monthly spending analysis
- Data visualisation through charts

### 💰 Budget Management
- Monthly budget creation
- Budget monitoring
- Spending progress tracking
- Budget-related insights

### 🤖 AI Expense Prediction
Money Mentor uses machine learning to analyse historical spending behaviour and predict future expenses.

The prediction system incorporates:

- Random Forest
- Gradient Boosting
- Ridge Regression
- Statistical trend analysis
- Moving averages

### 📄 Reports
- Expense report generation
- PDF export
- Financial data reporting

### 🌙 Additional Features
- Dark mode support
- Cloud-based data storage
- MVVM architecture
- REST API communication

---

## 🏗️ System Architecture

Money Mentor follows an **MVVM architecture** combined with a cloud-based application architecture.

```text
                    ┌─────────────────────┐
                    │    Android App      │
                    │ Kotlin + Compose    │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │    MVVM Layer       │
                    │ View / ViewModel    │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
     ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
     │   Firebase   │  │  Firestore   │  │ Flask ML API │
     │Authentication│  │   Database   │  │              │
     └──────────────┘  └──────────────┘  └───────┬──────┘
                                                  │
                                          ┌───────▼──────┐
                                          │  ML Models   │
                                          │ Random Forest│
                                          │ Gradient     │
                                          │ Boosting     │
                                          │ Ridge        │
                                          └───────┬──────┘
                                                  │
                                          ┌───────▼──────┐
                                          │    Render     │
                                          │ Cloud Hosting │
                                          └──────────────┘
```

---

## 🧠 AI & Machine Learning

The AI prediction component analyses users' historical expense data to estimate future spending.

### Machine Learning Models

| Model | Purpose |
|---|---|
| **Random Forest** | Captures non-linear relationships within expense data |
| **Gradient Boosting** | Improves prediction accuracy through sequential learning |
| **Ridge Regression** | Provides regularised regression for expense prediction |
| **Moving Average** | Identifies short-term spending trends |
| **Statistical Analysis** | Identifies historical spending patterns |

The machine learning models are implemented using **Python** and exposed through a **Flask REST API**.

The Android application communicates with the API to submit relevant expense data and receive prediction results.

---

## 🛠️ Technologies Used

### Android Development
- **Kotlin**
- **Android Studio**
- **Jetpack Compose**
- **MVVM Architecture**

### Backend & Cloud
- **Firebase Authentication**
- **Firebase Firestore**
- **Flask**
- **REST API**
- **Render**

### Machine Learning & Data Analytics
- **Python**
- **Random Forest**
- **Gradient Boosting**
- **Ridge Regression**
- **Statistical Analysis**
- **Moving Averages**

### Other Technologies
- SMS transaction parsing
- PDF/report generation
- Data visualisation
- Cloud computing

---

## 🔄 Application Workflow

```text
User
 │
 ▼
Login / Registration
 │
 ▼
Android Application
 │
 ├──────────────► Manual Expense Entry
 │
 └──────────────► Bank SMS Detection
                         │
                         ▼
                  SMS Transaction Parser
                         │
                         ▼
                  Expense Categorisation
                         │
                         ▼
                   Firestore Database
                         │
                         ▼
                 Expense Analytics
                         │
                ┌────────┴────────┐
                ▼                 ▼
          Visual Dashboard   ML Prediction
                                  │
                                  ▼
                           Flask ML API
                                  │
                                  ▼
                         Prediction Results
                                  │
                                  ▼
                           Android App
```

---

## 📱 Core Application Modules

### 1. Authentication Module
Handles user registration, login, authentication and profile management using Firebase Authentication.

### 2. SMS Expense Detection
Automatically identifies financial transactions from incoming bank SMS messages and extracts relevant information such as:

- Transaction amount
- Transaction type
- Merchant information
- Transaction date
- Expense category

### 3. Expense Management
Users can manually add, edit and manage their expenses while selecting appropriate categories.

### 4. Dashboard
Provides an overview of financial activity using statistics, charts and spending summaries.

### 5. Budget Management
Users can establish monthly budgets and monitor their spending against predefined limits.

### 6. AI Prediction
Historical expense data is processed by the machine learning API to generate future expense predictions.

### 7. Reporting
Users can generate and export financial reports in PDF format.

---

## 🔒 Security & Data Management

The application uses Firebase Authentication for user authentication and Firebase Firestore for cloud-based data storage.

The system is designed to separate user data and provide authenticated access to financial information.

> **Note:** This project is an academic prototype and should not be considered a production financial application. Real-world deployment would require additional security, privacy, compliance, encryption, and financial-data protection measures.

---

## ☁️ Deployment Architecture

The machine learning component is deployed using **Render**, allowing the Android application to communicate with the prediction service through a REST API.

```text
Android Application
        │
        │ HTTPS / REST API
        ▼
   Render Platform
        │
        ▼
    Flask API
        │
        ▼
Machine Learning Models
        │
        ▼
 Prediction Response
        │
        ▼
Android Application
```

---

## 📂 Project Structure

A simplified structure of the project is:

```text
Money-Mentor/
│
├── Android/
│   ├── app/
│   ├── src/
│   └── build.gradle
│
├── ML-API/
│   ├── app.py
│   ├── models/
│   ├── requirements.txt
│   └── ...
│
├── README.md
└── ...
```

> The exact structure may vary depending on the final project configuration.

---

## 🚀 Future Improvements

Potential future improvements include:

- Integration with additional banking services
- Improved SMS parsing for different banks
- More advanced deep learning models
- Personalised financial recommendations
- Improved prediction accuracy with larger datasets
- Real-time financial alerts
- Multi-currency support
- Enhanced financial security and encryption
- Cloud-based model retraining
- Web-based financial dashboard

---

## 🎓 Academic Context

This project was developed as a **Final Year Dissertation Project** for:

**BSc Computing (Network Engineering)**  
**University of Northampton – NAMI College**

The project demonstrates the integration of:

- Mobile application development
- Cloud computing
- Artificial intelligence
- Machine learning
- Data analytics
- REST API development
- Database management
- Software architecture

---

## 👩‍💻 Author

**Pratistha Katwal**

BSc Computing (Network Engineering)  
University of Northampton – NAMI College

---

## 📜 Disclaimer

Money Mentor was developed for **academic and educational purposes**. The application is a final-year dissertation prototype and should not be used as a substitute for professional financial advice or as a production financial management platform.