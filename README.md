# 🐍 Python Programming Course 

### Python Fundamentals → Data Analysis → Database → API Integration → Real-World Project

Ye ek **beginner-friendly, week-wise** Python programming course hai jo classroom mein parhane ke liye design kiya gaya hai. Har week mein **2 classes** hoti hain, aur har class ka apna folder hai jis mein `README.md` file hoti hai. Is file mein lecture notes, code examples aur practice questions hote hain.

Course ke end par students **API, Database, Pandas aur Matplotlib** ko combine karke ek **complete real-world data project** build karte hain.

---

## 📌 Table of Contents

- [Course Overview](#-course-overview)
- [Learning Outcomes](#-learning-outcomes)
- [Prerequisites](#-prerequisites)
- [Tools & Technologies](#-tools--technologies)
- [Course Roadmap](#-course-roadmap-8-weeks)
- [Projects](#-projects-jo-aap-banayenge)
- [Capstone Project](#-capstone-project-real-world-application)
- [Repository Structure](#-repository-structure)
- [Is Repository Ko Kaise Use Karein](#-is-repository-ko-kaise-use-karein)
- [Assessment Plan](#-assessment-plan)
- [Contact](#-contact)

---

## 📖 Course Overview

Is course mein student **zero programming knowledge** se start karke **real-world Python project** banana seekhta hai. Teaching ka approach practical hai:

- Har concept **real-life example** ke sath samjhaya jata hai
- Har topic ke sath **code examples** hote hain jo foran run kiye ja sakte hain
- Har class ke end par **scenario-based practice questions** hote hain
- Learning ko strong karne ke liye **mini-projects** aur ek **Capstone Project** hota hai

| Detail | Value |
|--------|-------|
| **Total Duration** | 2 Months (8 Weeks) |
| **Classes per Week** | 2 |
| **Total Classes** | 16 |
| **Level** | Beginner |
| **Platform** | Google Colab (primary) + VS Code (Capstone ke liye recommended) |

---

## 🎯 Learning Outcomes

Course ke end tak students ye sab kar sakein ge:

- ✅ Programming ke core concepts aur logic building samajhna
- ✅ Variables, data types, operators aur control flow use karna
- ✅ Lists, tuples, sets aur dictionaries ke sath kaam karna
- ✅ Functions aur modules se reusable code likhna
- ✅ Files aur JSON ke sath kaam karna, aur errors ko handle karna
- ✅ **NumPy** se numerical data par fast calculations karna
- ✅ **Pandas** se data load, clean aur analyze karna
- ✅ **Matplotlib** se charts aur visualizations banana
- ✅ **SQL ke basics seekhna aur SQLite database ke sath CRUD operations karna**
- ✅ **Existing public APIs se data fetch karna aur usay database / Pandas ke sath integrate karna**
- ✅ Git aur GitHub par apna project upload karna
- ✅ **API + Database + Data Analysis ka complete project build karna**

---

## ✅ Prerequisites

- Programming ka koi pehle se experience zaroori nahi hai
- Laptop aur internet connection
- Google account (Google Colab ke liye)
- Regular practice ka jazba

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|------|---------|
| [Google Colab](https://colab.research.google.com/) | Browser mein Python run karna (NumPy, Pandas, Matplotlib pehle se installed hain) |
| [VS Code](https://code.visualstudio.com/) | Code editor (Capstone project ke liye recommended) |
| [Python 3.x](https://www.python.org/downloads/) | Python interpreter |
| [NumPy](https://numpy.org/) | Numerical computing |
| [Pandas](https://pandas.pydata.org/) | Data analysis aur manipulation |
| [Matplotlib](https://matplotlib.org/) | Data visualization |
| [SQLite](https://www.sqlite.org/) | Lightweight database (Python mein built-in, `sqlite3` module) |
| [DB Browser for SQLite](https://sqlitebrowser.org/) | Database ko visually dekhne ke liye |
| [requests](https://requests.readthedocs.io/) | Public APIs se data fetch karne ke liye |
| [Git & GitHub](https://github.com/) | Version control aur project hosting |

---

## 🗓 Course Roadmap (8 Weeks)

| Week | Class 1 | Class 2 |
|:----:|---------|---------|
| **01** | [Programming Basics, Google Colab, Variables, Data Types, f-Strings & Arithmetic Operations](./Week-01/Class-01) | [User Input, Type Casting, Strings & Comparison/Logical Operators](./Week-01/Class-02) |
| **02** | Conditional Statements (`if`, `elif`, `else`) | Loops (`for`, `while`, `break`, `continue`) |
| **03** | Lists & Tuples | Sets & Dictionaries |
| **04** | Functions & Modules | File Handling, JSON & Exception Handling |
| **05** | **NumPy:** Arrays, Operations & Statistics | **Pandas:** Series, DataFrames, Data Cleaning & Analysis |
| **06** | **Matplotlib:** Line, Bar, Pie & Scatter Charts | **Database Basics:** SQL & SQLite (`CREATE`, `INSERT`, `SELECT`) |
| **07** | **Python + SQLite:** CRUD Operations & Pandas Integration | **API Integration:** `requests`, JSON, Public APIs → Database / Pandas |
| **08** | **Capstone:** Project Development & Git/GitHub | **Capstone:** Final Presentation & Review |

> 📝 *Links har week ka content publish hone ke sath activate hon ge.*

### 📅 Month-wise Breakdown

| Month | Weeks | Focus Area |
|-------|:-----:|------------|
| **Month 1** | 1 – 4 | **Fundamentals:** Variables, Operators, Control Flow, Data Structures, Functions, Files |
| **Month 2** | 5 – 8 | **Data & Integration:** NumPy, Pandas, Matplotlib, **Database**, **API Integration**, Capstone |

---

## 🚀 Projects Jo Aap Banayenge

| # | Project | Skills Applied | Week |
|:-:|---------|----------------|:----:|
| 1 | **Simple Calculator** | Variables, operators, user input | 1 |
| 2 | **BMI Calculator** | Arithmetic, conditionals, f-strings | 2 |
| 3 | **Number Guessing Game** | Loops, conditionals, `random` module | 2 |
| 4 | **Contact Book** | Dictionaries, loops, JSON file storage | 3–4 |
| 5 | **Student Marks Analyzer** | NumPy, Pandas | 5 |
| 6 | **Sales Data Dashboard** | Pandas, Matplotlib charts | 6 |
| 7 | **Student Database App (CLI)** | SQLite, CRUD operations | 7 |
| 8 | **Weather / Currency Fetcher** | Public API, `requests`, JSON, SQLite | 7 |
| 9 | **Capstone Project** | Poore course ka combined use | 8 |

---

## 🏆 Capstone Project: Real-World Application

Course ka final project ek **end-to-end data application** hoga. Ye real companies mein use hone wale **data pipeline** ka simple version hai:

```text
┌──────────────┐    requests     ┌──────────────┐    sqlite3    ┌──────────────┐
│ Public API   │ ──────────────▶ │   Python     │ ────────────▶ │   SQLite     │
│ (Weather,    │     JSON        │   Script     │   INSERT      │   Database   │
│  Currency…)  │                 │              │               │              │
└──────────────┘                 └──────────────┘               └──────┬───────┘
                                                                       │ SELECT
                                                                       ▼
                                                  ┌──────────────┐   Pandas   ┌──────────────┐
                                                  │  Matplotlib  │ ◀───────── │  NumPy /     │
                                                  │   Charts     │            │  Pandas      │
                                                  └──────────────┘            │  Analysis    │
                                                                              └──────────────┘
```

**Flow:** API se data fetch karo → database mein store karo → Pandas/NumPy se analyze karo → Matplotlib se visualize karo.

### Project Ideas (Students apni choice select karein)

| Project | API (Example) | Database Table | Analysis & Charts |
|---------|---------------|----------------|-------------------|
| **Weather Tracker & Analyzer** | [Open-Meteo](https://open-meteo.com/) | `weather_data` | Temperature trend line chart, average/max/min |
| **Currency Exchange Tracker** | [ExchangeRate-API](https://www.exchangerate-api.com/) | `exchange_rates` | Rate comparison bar chart |
| **Crypto Price Tracker** | [CoinGecko](https://www.coingecko.com/en/api) | `crypto_prices` | Price trend, % change analysis |
| **Country Explorer** | [REST Countries](https://restcountries.com/) | `countries` | Population / area comparison charts |
| **Expense Tracker** | [JSONPlaceholder](https://jsonplaceholder.typicode.com/) *(sample data)* | `expenses` | Category-wise pie chart, monthly summary |

> ⚠️ *API ki availability aur terms class se pehle check kar lein. Kuch APIs ko free API key chahiye hoti hai.*

### Capstone Requirements

- ✅ Kam az kam **1 public API** se data fetch karna
- ✅ Data ko **SQLite database** mein store karna (kam az kam 1 table)
- ✅ Database se data read karke **Pandas** mein analyze karna
- ✅ Kam az kam **2 charts** (Matplotlib) banana
- ✅ **Error handling** (API fail hone ya internet na hone par)
- ✅ Project **GitHub** par upload ho, sath mein achi `README.md` ho

---

## 📁 Repository Structure

```text
python-programming-course/
│
├── README.md                  # Main course overview (ye file)
│
├── Week-01/
│   ├── Class-01/
│   │   └── README.md          # Lecture notes, examples & practice questions
│   └── Class-02/
│       └── README.md
│
├── Week-02/
│   ├── Class-01/
│   │   └── README.md
│   └── Class-02/
│       └── README.md
│
├── ...
│
├── Week-05/                   # NumPy & Pandas
├── Week-06/                   # Matplotlib & Database
├── Week-07/                   # SQLite CRUD & API Integration
├── Week-08/                   # Capstone
│
├── Projects/                  # Projects ka complete source code
│
└── Resources/                 # Cheat sheets, SQL reference, extra reading
```

---

## 📚 Is Repository Ko Kaise Use Karein

1. Repository ko **clone** ya **download** karein.
   ```bash
   git clone https://github.com/<your-username>/python-programming-course.git
   ```
2. Current **Week** aur **Class** ka folder open karein.
3. Lecture content follow karne ke liye `README.md` parhein.
4. Saare code examples **Google Colab** ya **VS Code** mein khud run karein.
5. Har class ke end par diye gaye **Practice Questions** zaroor solve karein.
6. Apna kaam instructor ki hidayat ke mutabiq submit karein.

---

## 📊 Assessment Plan

| Component | Weight |
|-----------|:------:|
| Class Participation & Practice | 15% |
| Weekly Assignments | 20% |
| Mini-Projects | 20% |
| Mid-Term Evaluation (Week 4 ke baad) | 10% |
| Capstone Project | 35% |

---

