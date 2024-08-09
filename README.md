# SQL_Tabaleau_Dashboard ([Link](https://prod-apnortheast-a.online.tableau.com/#/site/mba24098876216f7b2/workbooks/2124522?:origin=card_share_link))

#### **1. Introduction to the Project**

**Objective:**
The project aims to develop a comprehensive Tableau dashboard to visualize and analyze sales data from AtliQ Hardware. Using MySQL for data extraction and analysis, the goal is to create interactive visualizations in Tableau that support business decision-making processes.

**Key Teams:**
- **Falcons:** The IT team responsible for managing the MySQL database and ensuring access for the Data Masters team.
- **Data Masters:** The data analysis team tasked with building the Tableau dashboard and interpreting the data insights.
- **Data Miners:** Although not directly involved in this project, they typically handle ETL (Extract, Transform, Load) processes in broader data projects.

#### **2. Project Planning with Aim's Grid**

**Purpose:**
To define and document the project's objectives, which include the creation of an interactive and insightful dashboard that provides actionable insights into sales performance.

**Stakeholders:**
- **Sales Team:** The primary users of the dashboard who will leverage the insights to make strategic decisions.
- **IT Team (Falcons):** Responsible for providing the database infrastructure and ensuring data integrity.
- **Data Analysis Team (Data Masters):** Charged with building the dashboard and performing the necessary data analysis.

**End Result:**
A fully functional Tableau dashboard that visualizes sales data and aids in decision-making by providing key insights into sales trends, customer behavior, and market performance.

**Success Criteria:**
- **Efficiency Improvement:** Reduce manual data processing time by 20%.
- **Sales Impact:** Potentially increase sales by 10% by providing actionable insights that enhance decision-making.

#### **3. Accessing and Analyzing MySQL Database**

**Setup:**
- **Installation:** MySQL and MySQL Workbench were installed to interact with the database.
- **Import Database:** The `db_dump.sql` file was downloaded and imported to set up the sales database on MySQL.

**Data Analysis Using SQL:**
- **Tables Examined:**
  - **Customers Table:** Contains columns for customer code, name, and type, providing basic customer information.
  - **Transactions Table:** Includes product code, customer code, market code, order date, sales quantity, sales amount, and currency. This table is crucial for sales analysis as it captures all transactional data.
  - **Products Table:** Lists products with identifiers, linking transactions to specific products.
  - **Markets Table:** Details market codes, city names, and zones, enabling analysis of sales performance by location.

- **Initial Queries:**
  - **Count Records:** Determined the number of records in the `transactions` and `customers` tables using `SELECT COUNT(*)`.
  - **Filtering:** Retrieved and analyzed transactions based on specific criteria (e.g., market code for Chennai) and performed aggregations, such as calculating total revenue.

**Challenges:**
- **Data Cleaning:** Addressed issues like negative sales amounts and currency inconsistencies (e.g., converting USD to INR). This involved data transformation and correction to ensure accurate analysis.

#### **4. Building the Tableau Dashboard**

**Dashboard Development:**
- **Data Connection:** Connected Tableau to the MySQL database to import and visualize the data.
- **Visualizations:**
  - **Sales Trends:** Created graphical representations of sales performance over time.
  - **Top Products and Customers:** Developed visualizations to highlight top-selling products and key customers.
  - **Revenue by Market:** Analyzed revenue distribution across various markets.

**Interactive Features:**
- **Filters:** Added filters to allow users to view data by specific regions (e.g., Delhi) or time periods (e.g., 2020). Filters were designed to update all relevant widgets on the dashboard, ensuring cohesive data visualization.

**Exporting and Sharing:**
- **PowerPoint Export:** Exported the dashboard to PowerPoint for inclusion in presentations. This captured the current view of the dashboard, making it easy to share specific insights.
- **Tableau Online Publishing:** Published the dashboard to Tableau Online, making it accessible via a web browser. This enabled managers and stakeholders to view the dashboard remotely without needing Tableau installed locally.

**Feedback and Iteration:**
- **Collect Feedback:** Gathered input from users to understand their needs and any issues encountered.
- **Version 2 Development:** Incorporated feedback to enhance the dashboard with additional features and insights, such as profit margins and more detailed analytics.

#### **5. Star Schema**

**Overview:**
The star schema is a database design model used in data warehousing to simplify and optimize data retrieval for analysis.

**Components:**
- **Fact Table:** The central table (e.g., `transactions`) that stores quantitative data (measures) such as sales amounts. It typically contains foreign keys linking to dimension tables.
- **Dimension Tables:** Surrounding tables (e.g., `customers`, `products`, `markets`) that store descriptive attributes related to the fact data. These tables provide context and enable detailed analysis.

**Implementation:**
- **Fact Table:** The `transactions` table serves as the fact table, storing sales data.
- **Dimension Tables:** The `customers`, `products`, and `markets` tables act as dimension tables, providing context to the sales transactions.

**Benefits:**
- **Simplified Queries:** The star schema’s straightforward structure simplifies SQL queries and enhances query performance.
- **Improved Analysis:** Facilitates efficient aggregation and filtering, making it easier to generate insightful reports and dashboards.
