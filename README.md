# Storage Aware Mechanism for IoT Applications 🔐

## Project Overview

This project addresses the critical challenge of securing sensitive data within Internet of Things (IoT) ecosystems. It proposes and implements a storage-aware mechanism that integrates security directly into data management. By leveraging a **Neo4j graph database**, the system understands and manages data based on its context, sensitivity, and usage, ensuring that data is protected from unauthorized access while maintaining the functionality and efficiency of the IoT network.

## 🚀 Features

  * **Graph Database Integration:** Utilizes a **Neo4j AuraDB** graph database to efficiently store and query complex, interconnected sensor data as nodes and relationships, which is ideal for dynamic IoT environments.
  * **Selective Data Uploading:** The system minimizes redundant data entries by implementing logic to check for changes in sensor readings before uploading, ensuring that only relevant changes are recorded.
  * **Dual-component Architecture:** The project is composed of a **Sensor Data Uploader** to insert data and a **Sensor Data Retriever** to fetch and display the data, simulating a real-time IoT network.
  * **Role-Based Access Control (RBAC):** Restricts data access based on user roles to minimize the risk of data breaches and enhance security.
  * **Scalable and Secure:** The system is designed to scale horizontally to handle large volumes of IoT data and incorporates security protocols like encryption to protect data in transit and at rest.

-----

## 🛠️ Technologies Used

  * **Database:** Neo4j Graph Database
  * **Language:** Python
  * **Libraries:** `neo4j-driver`, `threading`, `time`, `random`
  * **Security Concepts:** Role-Based Access Control (RBAC), Data Encryption (AES-256), TLS/SSL

-----

## ⚙️ Setup and Installation

Follow these steps to get the application up and running on your local machine.

### Prerequisites

  * Python 3.x
  * A Neo4j AuraDB instance with connection credentials.

### Dataset Information 📚

This project uses hardcoded, simulated sensor data points within the scripts to mimic a home IoT environment, so no external dataset file is required to run the application.

### 1\. Install Dependencies 📦

It is highly recommended to use a virtual environment to avoid conflicts.

```bash
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On macOS/Linux
source venv/bin/activate
# On Windows
.\venv\Scripts\activate

# Install the required Python packages
pip install neo4j
```

### 2\. Update Credentials and Run the Application ▶️

You must update the `uri`, `user`, and `password` variables in the provided Python scripts (`aura.py`, `AURADB.py`, `retrieve_data.py`, `sensor.py`) with your Neo4j AuraDB instance credentials before running.

You can run the uploader and retriever scripts separately or use the multithreaded approach in `AURADB.py`:

```bash
# To run the uploader and retriever concurrently
python AURADB.py

# To run the uploader script
python sensor.py

# To run the retriever script
python retrieve_data.py
```

-----

## 💬 Usage

  * **Simulate Data Flow:** Run the scripts to see data being uploaded to and retrieved from your Neo4j database.
  * **View Graph:** Log in to your Neo4j AuraDB instance to visualize the relationships between the `Room` and `Sensor` nodes that have been created.

-----

## ⚠️ Disclaimer

This application is provided for informational and demonstration purposes only. It is a simulation and should not be used as a substitute for professional security solutions in a real-world IoT environment.
