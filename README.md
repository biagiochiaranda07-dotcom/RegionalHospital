# Regional Hospital — Database Management Project

**A relational database project for modeling and managing a regional hospital information system.**

Regional Hospital is an academic database project that combines **PostgreSQL**, **PHP**, HTML, and conceptual database design. It explores how hospitals, departments, employees, patients, medical examinations, admissions, and clinical activities can be represented through a structured relational schema and accessed through a basic web interface.

## Project Scope

The modeled healthcare domain includes:

- **Hospitals and departments:** hospital identifiers, addresses, departments, personnel assignments, and department resources.
- **Medical and administrative staff:** doctors, nurses, administrative roles, departmental affiliations, and clinical responsibilities.
- **Patients and admissions:** patient records, ward admissions, and discharge-related information.
- **Examinations and laboratories:** internal and external outpatient facilities, examinations, associated costs, and special requirements.
- **Appointments:** examination bookings, dates, locations, and urgency-related information in the project specification.
- **Surgical activity:** operations, participating clinicians, and procedure stages.

These elements represent the project domain and accompanying schema; not every scenario is exposed through a finished web screen.

## Technology Stack

| Layer | Technology |
| --- | --- |
| Database | PostgreSQL |
| Server-side application | PHP (PostgreSQL extension) |
| Interface | HTML, CSS |
| Data modeling | Entity–Relationship diagrams, relational schema |
| Database backups | SQL schema and data exports |

## Database Design

The repository includes original and restructured E–R diagrams, a logical-schema document, PostgreSQL schema and data backups, and notes describing requirements and database behavior. The SQL schema models relationships among hospitals, wards, staff, patients, outpatient facilities, exams, and operations.

## Web Application

The PHP files demonstrate core database interactions:

- Registration and basic login flow.
- Viewing and querying stored information.
- Inserting, updating, and deleting records.
- Pages with sample queries involving doctors and surgical operations.

The repository contains exploratory and alternative PHP pages in addition to the primary screens.

## Repository Structure

```text
RegionalHospital-main/
├── backup_schema.sql               # PostgreSQL schema dump
├── backup_data.sql                 # Database data dump
├── creazione database.php          # Database creation script
├── autenticazione.html             # Login/registration entry page
├── login.php
├── registrazione.php
├── schermata_iniziale.php
├── insert.php
├── update.php
├── delete.php
├── Z_select.php                    # Additional SQL operations
├── Z_select_2.php
├── Z_insert_parte1.php
├── Z_insert_parte2.php
├── Z_update_parte1.php
├── Z_update_parte2.php
├── Z_delete_parte1.php
├── Z_delete_parte2.php
├── progetto (E-R).drawio
├── progetto (E-R ristrutturato).drawio
└── altro/                          # Requirements and design documents
```

## Local Setup (Development Only)

1. Install PostgreSQL, PHP, and the PHP PostgreSQL extension.
2. Create a local PostgreSQL database named `ospedali_regionali` using a dedicated, non-privileged development account.
3. Import `backup_schema.sql`; optionally import `backup_data.sql` if its sample records are appropriate for your environment.
4. Update the hard-coded connection strings in PHP files to match your local configuration; ideally, move these settings to environment variables.
5. Run the PHP application through a local development server, then access the authentication interface.

These steps describe the intended setup, **not a verified turnkey deployment**. The original application depends on database configuration and contains development-era code.

## Security Notice

**This is an educational prototype and must not be deployed publicly as-is.** The reviewed PHP code contains hard-coded database credentials and constructs at least some SQL queries through direct string concatenation of user input. Authentication also requires modernization.

Before considering deployment, remove exposed passwords from files and repository history, rotate them, use parameterized queries, hash user passwords, introduce authorization checks, and validate all inputs. Review `backup_data.sql` for real or sensitive personal information before publication; hospital-themed sample data should be synthetic or properly anonymized.

## Educational Value

This project demonstrates requirements analysis, conceptual and logical relational modeling, SQL schema design, database integrity concepts, and integrating PHP web forms with PostgreSQL CRUD operations.

## Author

**Biagio Chiarandà**

## License

No explicit license was included in the reviewed archive. Choose a license for the software and documentation if you wish to authorize reuse.
