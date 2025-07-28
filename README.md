# Cement Factory ERP System  
**Oracle Forms 11g / Reports & Oracle Database 12c**

A web‑deployed, fully integrated ERP for cement manufacturing operations—covering raw‐material procurement, production, quality control, inventory, dispatch, finance, HR, maintenance and reporting.


## 📖 Project Overview

This ERP system is built with Oracle Forms 11g and Reports, backed by an Oracle 12c database. It streamlines all critical cement‐factory workflows:

- **Secure Login & User Management**  
- **Raw Material Procurement & Inventory**  
- **Production Planning & Control**  
- **Quality Assurance & Lab Testing**  
- **Clinker & Cement Bagging**  
- **Dispatch & Logistics**  
- **Finance & Accounting**  
- **Human Resources & Payroll**  
- **Equipment Maintenance**  
- **Reports & Dashboards**


## 📂 Repository Contents

- `login_test.fmb` / `login_test.fmx`  
  — Login & authentication form  
- *(Additional `.fmb` / `.fmx` modules should be added here as you develop each feature)*


## 🏗️ Main Modules & Form Names

| Module                            | Form Source (`.fmb`)           | Form Executable (`.fmx`)          | Description                                                  |
|:--------------------------------- |:-------------------------------|:----------------------------------|:-------------------------------------------------------------|
| **Login**                         | `login_test.fmb`               | `login_test.fmx`                  | User authentication & role management                        |
| **Raw Material Inventory**        | `raw_materials.fmb`            | `raw_materials.fmx`               | Track limestone, gypsum, additives stock levels              |
| **Procurement**                   | `procurement.fmb`              | `procurement.fmx`                 | Purchase orders, vendor management                           |
| **Production Planning**           | `production_planning.fmb`      | `production_planning.fmx`         | Kiln scheduling, batch formulation                            |
| **Quality Control**               | `quality_control.fmb`          | `quality_control.fmx`             | Lab test entry: chemical & physical properties               |
| **Bagging & Dispatch**            | `bagging_dispatch.fmb`         | `bagging_dispatch.fmx`            | Bagging line control, dispatch orders & shipping             |
| **Inventory & Warehousing**       | `inventory.fmb`                | `inventory.fmx`                   | Finished goods, spare parts stock                            |
| **Finance & Accounting**          | `finance_accounts.fmb`         | `finance_accounts.fmx`            | Invoicing, ledger, payments, cost accounting                 |
| **HR & Payroll**                  | `hr_payroll.fmb`               | `hr_payroll.fmx`                  | Employee master, attendance, salary processing               |
| **Maintenance Management**        | `maintenance.fmb`              | `maintenance.fmx`                 | Preventive & breakdown maintenance scheduling                |
| **Reports & Dashboards**          | `reports_menu.fmb`             | `reports_menu.fmx`                | Generate operational, financial & compliance reports         |

> **Note:** You can import each `.fmb` into Oracle Forms Developer to compile or modify. Compiled `.fmx` files run on the Forms Server.


## 🛠️ Prerequisites

1. **Oracle Database 12c** (schema DDL scripts provided)  
2. **Oracle Forms 11g Developer & Runtime**  
3. **Oracle Reports 11g** (for `.rdf`/`.rep` report modules)  
4. **PL/SQL** for business logic triggers & procedures  
5. **Web listener / Forms server** configured to serve `.fmx` modules  


## 🚀 Installation & Deployment

1. **Database Setup**  
   - Execute `schema.sql` to create tables:  
     `USERS`, `MATERIALS`, `VENDORS`, `PRODUCTION`, `LAB_TESTS`, `BATCHES`, `INVENTORY`, `ORDERS`, `LEDGER`, `EMPLOYEES`, `MAINTENANCE_LOGS`, etc.  
   - Grant privileges to the Forms schema user.

2. **Compile Forms**  
   - Open each `.fmb` in Oracle Forms Developer → **Compile → Generate Form Module** → outputs `.fmx`.  
   - Place all `.fmx` files into your Forms Server deployment directory.

3. **Configure Forms Services**  
   - Add entries in `formsweb.cfg` (or equivalent) for each form module.  
   - Ensure `FORMS_PATH` includes the directory with your `.fmx` files.

4. **Configure Reports**  
   - Compile `.rdf`/`.rep` to `.fmx` or `.jar` as needed and register in Reports Server.

5. **Launch**  
   - Access via URL, e.g.:  
     ```
     http://<forms-server>:<port>/forms/frmservlet?config=default&form=login_test.fmx
     ```


## 🗄️ Database Schema Highlights

| Table                      | Purpose                                    |
|:---------------------------|:-------------------------------------------|
| `USERS`                    | Application users & roles                  |
| `RAW_MATERIALS`            | Limestone, gypsum, additives stock levels  |
| `VENDORS`                  | Supplier master data                       |
| `PROCUREMENT_ORDERS`       | Purchase orders & statuses                 |
| `PRODUCTION_BATCHES`       | Kiln batches, production timestamps        |
| `LAB_TESTS`                | Quality control test results               |
| `INVENTORY`                | Finished cement & spare parts              |
| `DISPATCH_ORDERS`          | Shipment orders & logistics                |
| `LEDGER`                   | Financial transactions                     |
| `EMPLOYEES`                | Staff master & employment details          |
| `PAYROLL`                  | Salary computation                         |
| `MAINTENANCE_LOGS`         | Equipment checks & service records         |

