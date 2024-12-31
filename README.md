# Automation Opportunity Analysis Project for Transurban

This project focuses on analysing automation opportunities for Transurban. Due to the confidentiality agreement with Transurban, I am unable to share all the datasets and detailed results publicly. However, I have included a summary of the analysis process to demonstrate the methodology and techniques used.

## About the Company
Transurban is a road operator that manages and develops urban toll road networks in Australia, Canada, and the United States and is considered one of the world's largest toll road operators. Their mission is to create roads that ensure lasting benefits to cities and their respective communities. Transurban is also a technology company that continuously researches and develops innovative tolling and transport technology that makes travel easier for everyone.

---

### Introduction
During my internship at Transurban, I had the privilege of working with the End User Automation team, a team dedicated to support teams for all Transurban employees by finding automation opportunities to enhance operational efficiency across the organisation to ensure that they can focus on more difficult tasks at hand. 

My primary task was to identify and analyse automation opportunities, particularly focusing on optimising workflows to reduce manual efforts and improve productivity. This report outlines the diagnostic analysis conducted on processes and this report highlights the methodologies and insights that informed my recommendations for improving efficiency and productivity. I will follow the steps of the data analysis process throughout the report: **ask, prepare, process, analyse, share, and act.**


## 1) Enhancing the Offboarding Process

### Ask
The primary objective of the project was to address inefficiencies in the mobile service offboarding process. The End User Automation team suspects that the company has been paying for unused mobile services even though the employees have left the company already, which had been causing delays, and additional costs and they weren’t sure what was causing the issue during the workflow process in the ServiceNow application, a software that automate business processes to streamline workflows and improve operation. The Data & Analytics team asks the team to analyse the user-device dependencies data in order to gain insight into how the workflow runs in the offboarding process.

<ins>Key Questions to Consider</ins>:
1. What are the major inefficiencies in the current mobile service offboarding process?
2. How do user-device dependencies contribute to delays or errors?
3. What improvements can be implemented to optimise the issue?
---

### Prepare
**Data Sources**
- Internal database: a primary data was provided by exporting data from ServiceNow, which includes:
  - Ticket logs and workflow information
  - Mobile service records detailing all users information, including existing and non-existing, and their mobile services
---
### Process
Since the data obtained is big and ambiguous, the tools used to process data will be Excel and R
- **Excel**:
  - Normalised user-device records to match data to their respective columns
  - Cross-referenced data using VLOOKUP
- **R**:
  - Removed duplicated entries
  - Extract Date into separated columns
  - Change column names for clarity
  - Grouped device type, user type
  - Grouped users who are still in the company and those who left to their respective mobile services
---
### Analyse
Based on the diagnostic analysis from the processed data, there are several points we can conclude:
1. The current workflow in ServiceNow is designed to disable only the services attached to mobile devices, rather than all services linked to a user's name. This limitation has resulted in unused services being overlooked. According to the company's standard, employees are allowed to have multiple mobile services for their roles. Consequently, when an employee is issued a mobile device, only the first service linked to the device is disabled. This leaves other services active, leading to unnecessary costs even after the employee has left the company.
2. Quantified redundancies, revealing a potential cost reduction of AUD 7,000 by addressing inefficiencies

---
### Share
**Visualisation**
- Created Tableau dashboards:
  - Illustrate the existing unused services where the employees has left the employee
  - Illustrate the existing unused services more than 6 months but the employees are still in the company
  - Visualise the cost of paying the unused services

**Deliverables**
- Created a presentation that includes:
  - Sharing findings wit the End User Automation team, including the breakdown of inefficiencies, the analysis process, and proposed solutions
  - Delivering Tableau dashboards and provided actionable insights

Now that the deliverables is prepared, a presentation was conducted to all the stakeholders to discuss about the possible solutions. We collaborated with the End User Enablement and Data & Analytics team to align recommendations with organisational goals. Received feedback on proposed changes, which were incorporated into the final workflow improvements.

---
### Act
After the discussion, these were the implementations were conducted:
1. Streamlined the offboarding process by redesigning the workflow to instead disable all services that is linked to the user's name
2. Transfer created Tableau dashboards into the ServiceNow dashboard and also deployed new dashboards for the HR's team

**Outcomes**
- Improved efficiency and accuracy of the mobile service offboarding process.
- Reduced AUD 7,000 operational cost by removing unused services
- Reduced overall workload by 20%, contributing to a more efficient and productive workflow.
- Enhanced decision-making with dynamic and real-time reporting tools (ServiceNow dashboard for the HR's team)








