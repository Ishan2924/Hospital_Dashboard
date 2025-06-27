# Hospital Operations Dashboard

## Outputs
![Screenshot 2025-06-27 173004](https://github.com/user-attachments/assets/d872a37b-a57c-47a8-977e-f1797dfb75ea)
<br>
![2](https://github.com/user-attachments/assets/2f4c5c2b-a747-4434-88ab-fc0e895bc2a3)
<br>
![3](https://github.com/user-attachments/assets/5a00a01f-c552-4941-aaf3-16207e48dc53)
<br>
![4](https://github.com/user-attachments/assets/e476ae8d-8d29-4238-bbe7-36177f015aee)
<br>
![5](https://github.com/user-attachments/assets/7b46ca47-a7f8-4e13-97c5-1217ef1c97be)
<br>
![6](https://github.com/user-attachments/assets/3b2fdbcd-37cb-4de3-b4d8-22846ac671e2)
<br>






This project delivers a comprehensive and interactive Hospital Operations Dashboard designed to provide deep insights into various facets of hospital management. Leveraging a robust MySQL backend for data integration and sophisticated analytical capabilities, this dashboard empowers stakeholders to monitor performance, identify trends, and make data-driven decisions across patient care, doctor performance, hospital operations, and financial health.

## Project Objective

The primary objective of this project is to transform complex, disparate hospital data into actionable intelligence. By consolidating data from multiple sources, this dashboard aims to:

* Streamline monitoring of key performance indicators (KPIs) across different hospital departments.

* Provide a holistic view of patient journeys, doctor activities, and facility utilization.

* Enable effective financial oversight and analysis.

* Facilitate quicker, more informed decision-making for improved operational efficiency and patient outcomes.

## Key Features

* **Centralized Data Management with MySQL:** Data from 16 disparate source tables were meticulously integrated and transformed into a streamlined, denormalized schema comprising just 7 core tables using advanced SQL joins and relational database practices.

* **Five Dedicated Analytical Pages:** The dashboard is structured into distinct, intuitively designed pages, each focusing on a critical area of hospital operations:

    * **Overview:** High-level summary of key hospital metrics and performance at a glance.

    * **Patient:** Detailed insights into patient demographics, admissions, discharges, and treatment pathways.

    * **Doctor:** Analysis of doctor performance, specialization trends, patient load, and efficiency.

    * **Hospital:** Operational metrics, resource utilization, bed occupancy, and departmental performance.

    * **Finance:** Comprehensive financial reporting, revenue analysis, expenditure tracking, and cost management.

* **Powerful Measures and DAX Queries:** Extensive use of calculated measures and Data Analysis Expressions (DAX) queries to derive complex KPIs, custom aggregations, and business logic, enabling deep analytical capabilities.

* **Rich Visualizations and Interactivity:** The dashboard utilizes a wide array of charts, graphs, tables, and slicers (e.g., bar charts, line graphs, pie charts, scatter plots, KPIs cards, heatmaps) to present data clearly and allow for dynamic exploration and drill-down capabilities.

* **Aesthetic and User-Friendly Design:** Incorporates custom images, backgrounds, and icons to create a visually appealing, professional, and intuitive user interface, enhancing the user experience.

## Technology Stack

* **Data Backend:** MySQL (for data consolidation, transformation, and storage)

* **Data Source:** Flat Files (CSV format, originating from Excel)

* **Dashboarding Tool:** Power BI (Implied by the use of DAX queries and visual capabilities)

* **Data Modeling & Analysis:** SQL (for data manipulation), DAX (for advanced calculations)

* **Visual Assets:** Custom images, icons, backgrounds

## Project Structure

```
Hospital_Dashboard/
├── excel/                   # Contains the raw or initially processed CSV files (from Excel)
│   ├── data_source_1.csv
│   ├── data_source_2.csv
│   └── ... (up to 16 original CSVs, or combined versions)
├── dashboard/               # Contains the main dashboard file
│   └── Hospital_Dashboard.pbix # Example for Power BI, adjust if using other tools
├── images/                  # Directory for all custom visual assets used in the dashboard
│   ├── icons/               # Custom icons for navigation, features, etc.
│   │   ├── icon1.png
│   │   └── ...
│   ├── doc_images/          # Images related to doctors, departments, or documentation
│   │   ├── doctor_profile.jpg
│   │   └── ...
│   ├── backgrounds/         # Full-page or section background images
│   │   ├── main_bg.jpg
│   │   └── ...
│   └── background_components/ # Smaller image elements or textures used in backgrounds
│       ├── gradient_overlay.png
│       └── ...
└── README.md                # This readme file

```
## Setup and Usage

To set up and interact with this dashboard locally, follow these general steps:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/Hospital_Dashboard.git](https://github.com/your-username/Hospital_Dashboard.git) # Replace with your actual repo URL
    cd Hospital_Dashboard
    ```

2.  **Set up MySQL Database:**

    * Ensure you have a MySQL server running locally or accessible.

    * Import the data from the CSV files located in the `excel/` directory into your MySQL database. You will need to create the 16 original tables first.

    * Execute the SQL scripts (if provided in the dashboard project) that perform the joins and transformations to reduce the 16 tables down to the 7 optimized tables, or manually construct these tables as per the dashboard's data model.

3.  **Open the Dashboard File:**

    * If using Power BI, ensure you have Power BI Desktop installed.

    * Open the `Hospital_Dashboard.pbix` file (or equivalent for your dashboarding tool) located in the `dashboard/` directory.

4.  **Connect to Data Source:**

    * Within the dashboard tool, update the data source connections to point to your local MySQL database. You may need to provide credentials.

    * Refresh the data to load the integrated information.

5.  **Explore the Dashboard:**

    * Navigate through the five distinct pages (Overview, Patient, Doctor, Hospital, Finance) using the dashboard's built-in navigation.

    * Interact with the filters, slicers, and visuals to explore the data and derive insights.

## Challenges & Key Learnings

* **Complex Data Integration:** A primary challenge involved designing and implementing efficient SQL joins across 16 raw tables to create a normalized, yet business-friendly, 7-table data model in MySQL. This required a deep understanding of relational database principles and query optimization.

* **Advanced DAX for Business Logic:** Developing intricate DAX measures was crucial for transforming raw data into meaningful business KPIs, handling time intelligence, and creating custom calculations that provided actionable insights.

* **Visual Storytelling:** The process of translating complex hospital data into clear, impactful, and visually appealing charts and dashboards required a strong focus on data visualization best practices and user experience design.

* **Resource Management:** Effectively managing and organizing a large number of visual assets (icons, backgrounds, images) within the project to ensure a consistent and high-quality aesthetic.

## Future Enhancements

* **Real-time Data Updates:** Implement automated data refresh mechanisms or direct connections to operational databases for near real-time insights.

* **Predictive Analytics Integration:** Incorporate machine learning models (e.g., for patient readmission prediction, resource demand forecasting) directly into the dashboard using integrated capabilities (e.g., Power BI's Python/R integration).

* **Custom Alerting System:** Develop a system for automated alerts based on predefined thresholds for critical KPIs (e.g., low bed occupancy, high patient wait times).

* **Role-Based Access Control:** Implement security measures to restrict access to specific dashboard pages or data based on user roles (e.g., finance, medical staff, administration).

* **Web Portal Deployment:** Deploy the dashboard as a web application or integrate it into a hospital's existing intranet portal for broader accessibility.

* **Advanced Drill-through Capabilities:** Enhance the ability to drill down from high-level summaries to individual record details for deeper investigations.
