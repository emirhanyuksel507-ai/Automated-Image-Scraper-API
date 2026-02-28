# 🤖 Automated Image Scraper & Database Manager

## 📌 Project Overview
This project is an automated Python pipeline designed to fetch, categorize, and download images from external APIs based on tasks stored in a local MySQL database. 

Instead of relying on fragile CSV files, this system uses a relational database for robust **State Management**. If the system is interrupted (e.g., power outage, network loss, or manual CTRL+C), it remembers exactly where it left off and resumes downloading the remaining files without any duplication.

## 🚀 Core Features
* **Database-Driven Workflow:** Reads search queries, target filenames, and folder names dynamically from a MySQL table.
* **Intelligent State Management:** Updates the `indirildi_mi` (is_downloaded) boolean flag in the database upon successful download. 
* **Crash Recovery:** Capable of resuming interrupted operations flawlessly.
* **Dynamic File Routing:** Automatically generates relative/absolute path directories and routes downloaded media into their respective categorized folders.
* **REST API Integration:** Communicates with external image APIs (Pexels / Pixabay / Google Custom Search) using authorized headers and JSON parsing.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Database:** MySQL (via XAMPP / WAMP)
* **Libraries:** `mysql-connector-python`, `requests`, `os`, `time`

## ⚙️ How to Setup and Run
1. Clone this repository to your local machine.
2. Import the `database_schema.sql` file into your local MySQL server to create the `stok_projesi` database and `gorseller` table.
3. Install required Python packages:
   ```bash
   pip install mysql-connector-python requests
