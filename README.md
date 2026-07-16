# ⚡ EcoFleet Solutions

<p align="center">

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge\&logo=postgresql\&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge\&logo=c\&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-003B57?style=for-the-badge)
![Database Design](https://img.shields.io/badge/Database-Design-2E8B57?style=for-the-badge)
![University Project](https://img.shields.io/badge/University-Project-blue?style=for-the-badge)

</p>

---

## 📖 Overview

**EcoFleet Solutions** is a PostgreSQL database project for a shared electric mobility platform.

The system models the main operations of an electric vehicle rental service, including fleet management, private and corporate clients, rentals, charging infrastructure, receipts, maintenance operations, technicians and certifications.

The project includes the full database design process, from requirements analysis and E-R modelling to the final relational schema and PostgreSQL implementation.
It also includes a small terminal-based C application that connects to the database through **libpq** and executes the main SQL queries.

---

## ✨ Main Features

* Conceptual E-R design
* Logical restructuring of the E-R schema
* Relational schema design
* PostgreSQL implementation
* Sample data population
* Domains and integrity constraints
* Primary keys and foreign keys
* Functions and triggers for operational consistency
* Indexes for query optimization
* Five representative SQL queries
* Command-line query client written in C

---

## 🏗️ Database Scope

The database manages:

* Electric vehicle fleet
* Vehicle subtypes: electric cars, electric vans, scooters and e-bikes
* Vehicle batteries
* Private and corporate clients
* Corporate employees
* Rental start and closure
* Payment receipts
* Charging hubs, stations and access points
* Maintenance operations
* Technicians and technical certifications

The database is designed to maintain consistency through relational constraints, domains, triggers and business rules.

---

## 🛠️ Technologies

| Technology    | Purpose                                   |
| ------------- | ----------------------------------------- |
| PostgreSQL    | Relational database                       |
| SQL           | Schema definition, population and queries |
| C             | Terminal-based client application         |
| libpq         | PostgreSQL client library for C           |
| E-R modelling | Conceptual database design                |

---

## 📂 Repository Structure

```text
.
├── README.md
├── sql/
│   └── ecofleet.sql
├── src/
│   └── query_all.c
└── docs/
    └── Relazione_Progetto_EcoFleet.pdf
```

---

## 📊 SQL Implementation

The file `sql/ecofleet.sql` contains the complete PostgreSQL implementation, including:

* domain definitions;
* table creation;
* primary keys, foreign keys and integrity constraints;
* data population;
* sequences;
* functions;
* triggers;
* indexes;
* final SQL queries.

The script is intended to be executed on an empty PostgreSQL database.

---

## 🔍 Example Queries

The implemented queries include:

* vehicle usage statistics by brand and model;
* private customers with total spending above a given threshold;
* rental analysis by hub city;
* vehicles currently under maintenance;
* battery usage ranking by recharge cycles.

---

## 💻 C Query Client

The file `src/query_all.c` contains a simple terminal-based C application that connects to PostgreSQL using `libpq`.

The program displays a textual menu and allows the user to execute the five main SQL queries.

Before compiling and running the program, the database connection parameters inside `query_all.c` should be adapted to the local PostgreSQL setup:

```c
#define PG_HOST "localhost"
#define PG_USER "postgres"
#define PG_DB "EcoFleet_DB"
#define PG_PASS "password"
#define PG_PORT 5432
```

The value `"password"` is only a placeholder.

---

## 📄 Documentation

The full project report is available in:

```text
docs/Relazione_Progetto_EcoFleet.pdf
```

The report is written in **Italian**, as the project was developed for an Italian university database course.

It includes:

* requirements analysis;
* conceptual design;
* E-R diagrams;
* logical design;
* redundancy analysis;
* relational schema;
* PostgreSQL implementation details;
* query definitions;
* index discussion;
* trigger description;
* C application overview.

---

## 🎓 Academic Context

This project was developed as part of the **Basi di Dati** course at the **University of Padua**.

The goal was to design, implement and document a relational database starting from a realistic application scenario, following the standard database design methodology.

---

## 👨‍💻 Authors

* Pietro Leonardo Acampora — [@hipietro](https://github.com/hipietro)
* Luca Artinian — [@ArtiLuca](https://github.com/ArtiLuca)
