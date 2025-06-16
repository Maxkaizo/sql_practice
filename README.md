# 🐘 SQL Practice Environment with Docker

This repository provides a Docker-based environment to practice SQL using PostgreSQL and PgAdmin. It is designed to support learning, controlled data loading, and query experimentation in a fully reproducible setup.

## 📦 Included Services

- **PostgreSQL** – The relational database engine for executing SQL queries and loading structured datasets.
- **PgAdmin 4** – A web-based UI for managing and exploring the PostgreSQL database.
- **(Optional)** Python scripts for controlled data ingestion, automation, and exploration (via Conda or Dockerized environments).

## 📁 Project Structure

```

sql\_practice/
├── docker-compose.yml         # Main Docker orchestration file
├── README.md                  # General project overview (this file)
├── README-notes.md            # Technical notes and setup decisions
├── data/
│   ├── persistent/            # Mounted volumes for data persistence
│   │   ├── postgres\_data/     # PostgreSQL internal data directory
│   │   └── pgadmin\_data/      # PgAdmin configuration and session files
│   ├── raw/                   # Unprocessed (downloaded) datasets
│   └── processed/             # Cleaned datasets ready for loading
├── sql/                       # Organized SQL scripts
│   ├── ddl/                   # Table creation and schema definitions
│   ├── dml/                   # Data manipulation (INSERT, UPDATE, etc.)
│   ├── queries/               # Analytical and practice queries
│   └── tests/                 # Data validation and test queries
├── src/                       # Python scripts for data handling
├── test/                      # Experimental notebooks or scripts
└── tmp/                       # Temporary files or scratch space

````

## 🚀 How to Start

Run the following command from the project root:

```bash
docker compose up --build
````

This will launch the PostgreSQL and PgAdmin containers and connect them in an isolated Docker network called `sqlnet`.

## 🔐 Default Credentials

* **PgAdmin**
  URL: [http://localhost:8080](http://localhost:8080)
  Email: `admin@example.com`
  Password: `admin`

* **PostgreSQL**
  Host: `localhost`
  Port: `5432`
  User: `myuser`
  Password: `mypassword`
  Default Database: `mydb`

> You can change these values in the `.env` file.

## 📖 Additional Notes

For implementation details, configuration decisions, and troubleshooting steps, refer to [`README-notes.md`](./README-notes.md).

