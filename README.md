# Automated Data Integration with Bash and GitHub Actions

## Project Overview  
This project addresses inefficiencies in the manual data integration processes used by the data analysts at the TDI community. These processes involve consolidating approximately 10,000 new applications submitted daily by individuals seeking enrollment in specific cohorts. The manual approach has caused significant delays in analysis and decision-making.

As a data scientist, your task is to design and implement an automated solution to streamline the integration process, ensuring efficiency, accuracy, and scalability.

---

## Objective  
The goal is to automate the data integration process using **Bash scripting** and **GitHub Actions**. This solution will process large volumes of incoming applications, consolidate datasets, and minimize delays caused by manual tasks.

---

## Key Requirements  

### 1. Integration of Datasets  
- **Input:** There are three distinct datasets located in the `data-hub` folder.  
- **Task:** These datasets need to be merged into a single consolidated data file.  

### 2. Storage of Output  
- **Output:** The final integrated data file will be saved in the `db` folder within the project directory.  

### 3. Handling New Data  
- **Detection:** The system should detect the arrival of new data (use one of the datasets as a test case).  
- **Automation:** GitHub Actions will automatically trigger the data integration process whenever new data is detected.  
- **Update:** The `db` folder will be updated with the latest integrated data.  

### 4. Output Validation  
- Ensure the final integrated file in the `db` folder is accurate and reflects all available data.  

---

## Expected Outcomes  
- Automation of the data integration process to save time and improve efficiency.  
- Elimination of delays caused by manual integration processes.  
- Scalable and robust solution to handle the growing data volume effectively.  

---

## Implementation Steps  

### 1. **Dataset Integration Script**  
- Develop a **Bash script** to:  
  - Read datasets from the `data-hub` folder.  
  - Consolidate them into a single data file.  
  - Validate the merged dataset for completeness and accuracy.  

### 2. **Automated Workflow with GitHub Actions**  
- Create a GitHub Actions workflow to:  
  - Monitor changes in the `data-hub` folder for new data files.  
  - Automatically trigger the Bash integration script upon detecting updates.  
  - Push the updated consolidated file to the `db` folder.  

### 3. **Testing the Solution**  
- Simulate the arrival of new data in the `data-hub` folder to ensure the automation triggers and performs as expected.  

---

## File Structure  

```plaintext
project-directory/
│
├── data-hub/        # Contains input datasets
│   ├── dataset1.csv
│   ├── dataset2.csv
│   └── dataset3.csv
│
├── db/              # Stores the consolidated output file
│   └── integrated_data.csv
│
├── scripts/         # Bash scripts for data integration
│   └── integrate_data.sh
│
├── .github/
│   └── workflows/   # GitHub Actions configuration
│       └── data_integration.yml
│
└── README.md        # Project documentation

