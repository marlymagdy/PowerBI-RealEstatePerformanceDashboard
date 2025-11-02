Absolutely 👍 here’s the **final README file**, fully formatted and ready for direct copy-paste into GitHub — everything clean, consistent, and professional:

---

## 📊 Project Overview

This Power BI dashboard provides a comprehensive view of **real estate business performance** by connecting multiple datasets — **Client**, **Expense**, **Property**, and **Sales** — to deliver actionable insights across revenue, income, property sales, and client activity.

The dashboard focuses on tracking **revenue growth**, analyzing **top-performing properties**, and visualizing **client contributions** using interactive visuals and DAX-driven KPIs.

---

## 🖼️ Dashboard Preview

*(Add your dashboard image below)*
![Real Estate Dashboard](path_to_your_image.png)

---

## 🧩 Data Model

The project integrates four main tables:

* **Client:** Client details including name, image, and occupation
* **Expense:** Expense records associated with properties and operations
* **Property:** Property details such as type, price, city, and country
* **Sales:** Sales transactions with payment status and revenue data

A **Calendar table** was created for accurate time intelligence and to support date-based filtering:

```DAX
Calendar =
ADDCOLUMNS(
    CALENDARAUTO(),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date], "mmm"),
    "Monthnum", MONTH([Date]),
    "Day", DAY([Date]),
    "Weekday", FORMAT([Date], "ddd"),
    "Weeknum", WEEKDAY([Date]),
    "Qtr", "Q" & FORMAT([Date], "Q"),
    "WeekType", IF(WEEKDAY([Date]) = 1 || WEEKDAY([Date]) = 7, "Weekend", "Weekday")
)
```

---

## ⚙️ DAX Measures

A series of DAX measures were developed to power key insights and visuals:

| **Measure**               | **Description**                                                    |
| ------------------------- | ------------------------------------------------------------------ |
| **Revenue**               | Total revenue generated from property sales                        |
| **Expense**               | Total operational and property-related expenses                    |
| **Income**                | Calculated as Revenue – Expense                                    |
| **Revenue PY**            | Revenue for the previous year (used for year-over-year comparison) |
| **Revenue Growth %**      | Percentage growth in revenue compared to the previous year         |
| **Revenue Growth color**  | Dynamic color indicator based on growth direction                  |
| **Max_min Revenue color** | Highlights highest and lowest revenue values                       |
| **Properties sold**       | Total number of sold properties                                    |
| **Payment Status SVG**    | SVG-based visual indicator of payment completion                   |
| **% GT**                  | Percentage contribution to the grand total                         |

---

## 📈 Key Insights

* Revenue, Expense, and Income visualized with year-over-year growth tracking
* Top clients displayed using images, names, occupations, and revenue in a table visual
* Property performance by type, location, and country
* Sunburst chart highlighting the top 3 occupations by property type
* Payment tracking with SVG indicators to show status clearly
* Calendar-based filtering enabling smooth navigation between years *(2022–2024)*

---

## 🧠 Skills Demonstrated

* Advanced **Power BI Data Modeling**
* **DAX** for dynamic KPIs and year-over-year comparisons
* **Interactive visuals** (Cards, Column Charts, Tables with Images, Sunburst, SVG indicators)
* **Data storytelling** with clear and professional dashboard design

---



