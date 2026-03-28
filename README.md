# Layoffs Data Analysis & Cleaning | MySQL

A structured SQL project focused on cleaning, transforming, and analysing a real-world layoffs dataset to uncover trends across industries, companies, and years.

## 📋 Project Overview

This project involves end-to-end data processing using MySQL — from removing duplicates and handling nulls to performing exploratory data analysis (EDA) on global layoff trends.

---

## 🛠️ Tools & Technologies

- **MySQL** — Data cleaning & analysis
- **SQL Concepts** — CTEs, Window Functions, Joins, Aggregations, String Functions

---

## 🔧 Steps Performed

### 1. Removed Duplicates
- Created a staging table to preserve raw data
- Used `ROW_NUMBER()` with `PARTITION BY` to identify and delete duplicate records

### 2. Standardized the Data
- Trimmed whitespace from company names
- Unified inconsistent industry labels (e.g., all `Crypto%` → `Crypto`)
- Removed trailing punctuation from country names
- Converted date strings to proper `DATE` format using `STR_TO_DATE()`

### 3. Handled Null & Blank Values
- Used self-joins to fill missing industry values from matching company records
- Deleted rows where both `total_laid_off` and `percentage_laid_off` were null

### 4. Removed Unnecessary Columns
- Dropped the helper `row_num` column after cleaning was complete

---

## 📊 Exploratory Data Analysis

- Identified maximum layoffs and 100% layoff companies
- Aggregated total layoffs by **industry**, **company**, and **year**
- Computed **rolling monthly totals** using window functions
- Ranked **top 5 companies** by layoffs per year using `DENSE_RANK()`

---

## 💡 Key Insights

- Tracked layoff trends from 2020 to 2023 across multiple industries
- Identified the most impacted sectors and companies year over year
- Built a rolling total to visualise cumulative layoffs over time

---

Built with ❤️ using MySQL
