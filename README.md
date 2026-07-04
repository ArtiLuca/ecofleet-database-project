# ecofleet-database-project
PostgreSQL database project for a shared electric mobility platform, including E-R design, SQL implementation, triggers, indexes and a C/libpq query client.

# EcoFleet Solutions — PostgreSQL Database Project

EcoFleet Solutions is a relational database project for a shared electric mobility platform.

The system models the main operations of an electric vehicle rental service, including fleet management, private and corporate clients, rentals, charging infrastructure, receipts, maintenance operations, technicians and certifications.

The project includes a full PostgreSQL implementation and a small C terminal application for executing the main SQL queries through `libpq`.

## Repository Structure

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

## Features

- Conceptual E-R design and logical restructuring
- Relational schema design
- PostgreSQL schema creation
- Database population with sample data
- Integrity constraints, primary keys and foreign keys
- Indexes for query optimization
- Functions and triggers for operational consistency
- Five representative SQL queries
- C query client using PostgreSQL `libpq`

## Tech Stack

- PostgreSQL
- SQL
- C
- libpq
- E-R modelling
- Relational database design

## Database Scope

The database manages:

- electric vehicles, including cars, vans, scooters and e-bikes
- vehicle batteries
- private and corporate clients
- rental start and closure
- receipts for completed rentals
- charging hubs, stations and access points
- maintenance operations
- technicians and technical certifications

## SQL Implementation

The main SQL file is:

```text
sql/ecofleet.sql
```

It contains the complete PostgreSQL implementation, including table creation, data population, sequences, functions, triggers, indexes and the final project queries.

The script is intended to be executed on an empty PostgreSQL database.

## C Query Client

The file:

```text
src/query_all.c
```

contains a terminal-based C application that connects to the PostgreSQL database using `libpq`.

The program displays a menu and allows the user to execute the five main SQL queries.

Before compiling and running the program, the connection parameters inside `query_all.c` should be adapted to the local PostgreSQL setup:

```c
#define PG_HOST "localhost"
#define PG_USER "postgres"
#define PG_DB "EcoFleet_DB"
#define PG_PASS "password"
#define PG_PORT 5432
```

The value `"password"` is only a placeholder.

## Documentation

The full project report is available in:

```text
docs/Relazione_Progetto_EcoFleet.pdf
```

The report is written in **Italian**, as the project was developed for an Italian university database course.

It includes the requirements analysis, conceptual design, logical design, redundancy analysis, relational schema, PostgreSQL implementation details, query definitions, index discussion, trigger description and C application overview.


