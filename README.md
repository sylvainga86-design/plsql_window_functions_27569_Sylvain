STEP 1 :  Problem definition. 
 
Business Context 
  
A hospital created a Hospital Management System analyzing the number of patient 
visits, the type of medical services, and the hospital billing to enhance efficiency and 
patient care. 
  
Industry: Healthcare 
  
Department: Hospital Administration & Finance 
  
Data Challenge 
  
Information on patients, services, and billing are kept in different tables. And this 
becomes a challenge to find out the service utilization, the information on patients, and 
the income growth over time. 
  
Expected Outcome 
   
Determine easly the type and quality of a service that the patient received according to 
price he/she paid, keeping track of the hospital’s revenues and incomes over time easly 
and effitiently, And helping in taking sttrategic and wised decisions in the allocation of 
recources. 
 
Step 2: Success Criteria. 
 
▪  Compute running monthly hospital revenue - SUM() OVER() 
▪  Calculate 3-month moving average revenue - AVG().OVER() 
▪  Measure month-over-month revenue growth - LAG() 
▪  divide patients into spending groups - NTILE(4) 
▪  Identify Top 5 medical services per department - RANK() 
 
 
 
STEP 3: Database Schema Design 
 
 
STEP 4: PART A — SQL JOINs Implementation 
 
INNER JOIN — Valid Visits 
 
 
Business Interpretation 
Displays confirmed hospital visits linked to registered patients and services, ensuring 
reliable billing analysis. 
 
LEFT JOIN — Patients with No Visits 
 
 
Interpretation: 
Identifies registered patients who have never visited the hospital. 
 
 
 
 
RIGHT JOIN — Services Never Used 
 
 
Interpretation: 
Highlights medical services that have not been utilized. 
 
 
 
 
 
 
FULL OUTER JOIN — Patients & Services 
 
 
Interpretation: 
Compares all patients and services, including unmatched records. 
 
SELF JOIN — Patients from Same Region 
 
 
Interpretation: 
Helps analyze patient distribution within the same region. 
 
STEP 5: PART B — Window Functions 
 
Ranking Functions — Top Services by Revenue 
 
Interpretation: 
Ranks medical services within each department based on revenue. 
 
 
 
 
Aggregate Window — Running Revenue 
 
Interpretation: 
Shows cumulative hospital revenue growth over time. 
 
Navigation Function — Month-to-Month Growth 
 
Interpretation: 
Tracks changes in revenue between consecutive periods. 
 
 
 
 
 
 
 
Distribution Functions — Patient Segmentation 
 
Interpretation: 
Segments patients into quartiles based on hospital spending. 
 
Moving Average (3-Month) 
 
Interpretation: 
Smooths revenue trends to support forecasting.
STEP 7: Results Analysis 
 
Descriptive 
Hospital revenue increased steadily, with diagnostics and surgery services generating 
the highest income. 
Diagnostic 
A small group of patients contributes significantly to total revenue, while some services 
remain underutilized. 
Prescriptive 
Promote underused services, optimize staffing in high-demand departments, and 
introduce loyalty programs for high-value patients. 
 
STEP 8: References 
▪  Oracle SQL Window Functions Documentation 
▪  PostgreSQL Analytical Functions Guide 
▪  W3Schools SQL JOINs 
 
All sources were properly cited. Implementations and analysis represent original 
work. No AI-generated content was copied without attribution or adaptation. 
