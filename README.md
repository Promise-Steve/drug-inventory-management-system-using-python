#  Drug Inventory Management System

### Python-Based Inventory Analysis and Decision-Support Prototype

A Python-based Drug Inventory Management System developed to analyse **simulated medicine inventory data**, identify inventory risks, calculate inventory indicators, and generate information that can support inventory-management decisions.

---

##  Project Overview

Medicine inventory management requires timely information about stock availability, inventory value, expiry risk, and potential overstocking.

This project demonstrates how a Python-based analytical system can transform structured inventory records into actionable information for inventory-management decision-making.

The project follows the analytical workflow:

**Data → Validation → Processing → Analysis → Risk Identification → Management Summary → Stakeholder Action**

The system is designed as an **educational and portfolio prototype** and should not be considered a replacement for professional pharmaceutical inventory-management systems.

---

##  Business Questions

The analysis was designed to answer the following practical inventory questions:

1. How many medicines are being tracked?
2. What is the total inventory value?
3. Which medicines are low stock?
4. Which medicines are critically low?
5. Which medicines are overstocked?
6. Which medicine has the highest inventory value?
7. Which medicine has the lowest stock?
8. How is inventory distributed across facilities?
9. Which medicines are approaching expiry?
10. Which inventory issues require management attention?
11. What actions should stakeholders consider based on the findings?

---

##  Dataset

The project uses a **simulated medicine inventory dataset created directly in Python**.

Each inventory record contains information such as:

* Drug ID
* Drug name
* Category
* Facility
* Quantity
* Reorder level
* Maximum stock
* Unit price
* Supplier
* Expiry date

The dataset contains:

* **28 total records**
* **25 valid inventory records**
* **3 intentionally invalid records**

The invalid records were deliberately included to demonstrate the importance of **data validation before analysis**.

###  Important Dataset Note

This is a **simulated dataset** created for educational, analytical, and portfolio purposes.

It does **not** represent real patients, hospitals, pharmacies, healthcare facilities, pharmaceutical companies, or real-world inventory records.

No personal or confidential information is contained in the dataset.

---

##  Data Validation

Before conducting the analysis, the inventory records were checked for common data-quality problems.

The validation process identified:

* Negative quantities
* Negative unit prices
* Missing medicine names
* Maximum stock levels below reorder levels

After validation:

**25 valid records** were retained for analysis, while **3 invalid records** were excluded.

This demonstrates an important principle in data analysis:

> **Reliable analysis begins with reliable data.**

---

##  Analytical Approach

The system calculates and evaluates several inventory indicators.

### Inventory Value

The inventory value of each medicine is calculated as:

```text
Inventory Value = Quantity × Unit Price
```

### Stock Classification

Medicines are classified using the following rules:

| Classification | Rule                               |
| -------------- | ---------------------------------- |
| Critical Stock | Quantity ≤ 50% of reorder level    |
| Low Stock      | Quantity ≤ reorder level           |
| Overstocked    | Quantity > maximum stock           |
| Adequate       | Does not meet the conditions above |

### Near-Expiry Monitoring

Medicines with **30 days or fewer remaining before expiry** are identified as near-expiry medicines.

The analysis uses:

**Analysis date: 16 September 2026**

---

##  Key Results

Analysis of the 25 validated inventory records produced the following results:

| Indicator                |         Result |
| ------------------------ | -------------: |
| Total inventory records  |         **25** |
| Invalid records excluded |          **3** |
| Healthcare facilities    |         **12** |
| Total units in inventory |      **7,890** |
| Total inventory value    | **₦2,009,950** |
| Average inventory value  |    **₦80,398** |
| Average unit price       |    **₦439.60** |
| Low-stock medicines      |          **5** |
| Critical-stock medicines |          **4** |
| Overstocked medicines    |          **3** |
| Near-expiry medicines    |          **4** |

---

##  Key Analytical Findings

### 1. Low-Stock Medicines

**5 medicines** were classified as low stock based on the defined reorder-level criterion.

These medicines require review by pharmacy and procurement teams to determine appropriate replenishment needs.

The identified low-stock medicines were:

* **DRG002 — Amoxicillin 500mg**
* **DRG006 — Ciprofloxacin 500mg**
* **DRG013 — Salbutamol Inhaler**
* **DRG016 — Azithromycin 500mg**
* **DRG022 — Doxycycline 100mg**

### 2. Critical-Stock Medicines

**4 medicines** were classified as critical stock.

These medicines had quantities at or below 50% of their defined reorder levels and may require urgent inventory review.

The identified critical-stock medicines were:

* **DRG004 — ORS Sachets**
* **DRG008 — Insulin**
* **DRG011 — Ceftriaxone Injection**
* **DRG017 — ORS Sachets**

### 3. Overstocked Medicines

**3 medicines** were classified as overstocked:

* **DRG007 — Ibuprofen 400mg**
* **DRG014 — Hydrochlorothiazide**
* **DRG019 — Folic Acid**

These records indicate inventory levels above their defined maximum-stock thresholds.

### 4. Near-Expiry Medicines

**4 medicines** were identified as near expiry using the 30-day threshold.

These included:

* **DRG004 — ORS Sachets**
* **DRG008 — Insulin**
* **DRG011 — Ceftriaxone Injection**
* **DRG017 — ORS Sachets**

These records combine inventory concerns with approaching expiry dates and therefore warrant prompt review.

### 5. Highest-Value Medicine

**DRG003 — Artemether/Lumefantrine** had the highest inventory value among the 25 valid records.

* Quantity: **850 units**
* Unit price: **₦450**
* Inventory value: **₦382,500**

---

##  Management Implications

The analysis provides information that can support practical decision-making by:

* Pharmacy and inventory managers
* Procurement officers
* Facility managers
* Health-system decision-makers

Potential management actions include:

### Pharmacy & Inventory Managers

* Monitor low-stock and critical-stock medicines.
* Review medicines approaching expiry.
* Monitor overstocked medicines.
* Apply appropriate stock rotation and inventory-control practices.

### Procurement Officers

* Review critical and low-stock medicines during replenishment planning.
* Avoid unnecessary procurement of medicines that are already overstocked.
* Consider current inventory levels when making purchasing decisions.

### Facility Managers

* Review medicine availability within facilities.
* Coordinate with pharmacy and procurement teams when shortages or excess stock are identified.
* Consider appropriate redistribution of stock where permitted.

### Health-System Decision-Makers

* Use inventory summaries to identify supply-management issues.
* Support coordinated procurement and distribution decisions.
* Encourage regular monitoring of stock levels, expiry dates, and inventory value.

---

##  Technologies Used

* **Python**
* **Jupyter Notebook**
* **Python dictionaries and lists**
* **Functions**
* **Conditional logic**
* **Loops**
* **Data validation**
* **Inventory calculations**
* **Search functionality**
* **Decision-support logic**

---

##  Repository Structure

```text
drug-inventory-management-system-using-python/
│
├── data/
│   └── README.md
│
├── drug_inventory_management.ipynb
│
└── README.md
```

The main analytical work is contained in:

```text
drug_inventory_management.ipynb
```

The notebook includes the simulated dataset, validation procedures, inventory calculations, analytical functions, interactive menu, inventory summary, and stakeholder-action section.

---

##  Core System Features

The interactive Python system provides functionality for:

1. **View Inventory**
2. **Search Medicine**
3. **Identify Low-Stock Medicines**
4. **Identify Critical-Stock Medicines**
5. **Identify Overstocked Medicines**
6. **Identify Near-Expiry Medicines**
7. **Generate Inventory Summary**
8. **Exit the System**

---

##  Reproducibility

The project is self-contained.

The simulated dataset is created within the Jupyter notebook, meaning users can open the notebook and reproduce the analysis without requiring access to an external database or confidential healthcare dataset.

To reproduce the project:

```bash
git clone https://github.com/Promise-Steve/drug-inventory-management-system-using-python.git
```

Then open:

```text
drug_inventory_management.ipynb
```

in Jupyter Notebook or JupyterLab.

---

##  Future Improvements

Future versions of the system could include:

* Integration with a real inventory database
* Automated stock alerts
* Automated expiry notifications
* Consumption-rate analysis
* Reorder recommendations
* Supplier performance analysis
* Facility-to-facility stock redistribution
* Interactive dashboards
* Database integration
* Streamlit web-app deployment
* Automated testing
* Role-based access control

---

##  Disclaimer

This project is an **educational and portfolio prototype** based on simulated data.

The inventory thresholds and analytical rules used in the project are simplified assumptions developed for demonstration purposes.

The system should not be used as a substitute for professional pharmaceutical inventory-management procedures, clinical judgement, regulatory requirements, or validated healthcare supply-chain systems.

---

##  Project Focus

This project demonstrates practical application of:

**Python • Data Validation • Data Analysis • Inventory Analytics • Healthcare Data • Decision Support • Problem Solving • Business Intelligence • Process Improvement**

---

###  Project Objective

The broader objective of this project is to demonstrate how relatively simple Python-based analytical tools can convert structured inventory data into information that helps stakeholders identify **stock shortages, critical inventory risks, overstocking, expiry risks, and inventory-value considerations**.
