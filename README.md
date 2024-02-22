Lucerne Festival Data Extraction and PostgreSQL Interaction

Description

This repository contains Python scripts for extracting event details from the Lucerne Festival website and interacting with a PostgreSQL database to store and manage the extracted data. The process involves:
1.	Data Extraction: The script extracts event details such as title, venue, date, time, artists, programs, and image links from the Lucerne Festival website. It iterates through event links and retrieves information for each event. The extracted data is stored in a Pandas DataFrame and exported to a CSV file named "lucerne_festival_data.csv".
2.	Inserting into PostgreSQL: Python code is provided to interact with a PostgreSQL database and perform the following tasks:
•	Create tables for storing event-related data.
•	Insert unique values into separate tables for venues, artists, programs, and titles.
•	Update a DataFrame with corresponding IDs from the database tables.
•	Optionally, insert data from the updated DataFrame into the events table.
Prerequisites

•	Python 3 installed on your system.
•	PostgreSQL database server running locally or remotely, accessible via Python's psycopg2 library.
•	Basic knowledge of SQL and Python programming.
•	
Setup Instructions

1. Install Required Python Packages
Install the required Python packages using pip:

-- pip install pandas psycopg2-binary 

2. PostgreSQL Installation
a. Download PostgreSQL
Visit the official PostgreSQL website and download the appropriate installer for your operating system.
b. Install PostgreSQL
Run the downloaded installer and follow the installation wizard's instructions. Make sure to remember the password you set for the default postgres user during installation.

3. pgAdmin Installation
a. Download pgAdmin
Go to the pgAdmin download page and download the installer for your operating system.
b. Install pgAdmin
Run the downloaded installer and follow the installation wizard's instructions.

4. Connect to PostgreSQL Database
a. Launch pgAdmin
Open pgAdmin from your computer's applications menu or desktop shortcut.
b. Add Server
In pgAdmin, click on the "Add New Server" button or right-click on "Servers" in the left sidebar and select "Create" > "Server..."
c. Enter Connection Details
Fill in the following details:
•	Name: A friendly name for your server.
•	Host name/address: localhost if PostgreSQL is running on the same machine; otherwise, enter the IP address or hostname of your PostgreSQL server.
•	Port: 5432 is the default port for PostgreSQL.
•	Username: postgres (default username).
•	Password: Enter the password you set during PostgreSQL installation.
d. Save Connection
Click "Save" to save the connection settings.
e. Connect to Server
Double-click on the server you just added to connect to the PostgreSQL database.

Docker Configuration
For Docker deployment, Dockerfiles and a docker-compose file are provided in this repository. Please refer to Dockerfile.df and docker-compose.yml for configuring and deploying the application using Docker.
Connection Details in Code
The connection details in the Python code are as follows:
•	User: postgres
•	Password: postgres
•	Host: localhost
•	Port: 5432
•	Database: docker