# Tableau Dashboard: HR Analytics Attrition Rate

![](https://media.licdn.com/dms/image/v2/D5612AQEYDlxdxPtVdA/article-cover_image-shrink_720_1280/article-cover_image-shrink_720_1280/0/1714496385288?e=2147483647&v=beta&t=IUh83dzNu9llrMafXRBT273KsiuU0wg03eMCdYpSgOs)

This project is aimed at creating a dashboard in Tableau to visualize key statistics and factors affecting employee attrition within an organisation. Employee attrition rate is often of interest to an organization’s Human Resources (HR) department. 

![](https://github.com/user-attachments/assets/dfbb863c-1d13-4add-a670-cfa35837d635)

## Data Source

This data visualization task was inspired by [this](https://www.kaggle.com/datasets/anshika2301/hr-analytics-dataset) HR Analytics project. It comprises a [dataset](https://drive.google.com/drive/folders/18mQalCEyZypeV8TJeP3SME_R6qsCS2Og) containing information on 1,470 employees within an organisation, such as their job role, monthly income, performance ratings and whether they have attrited or not.  

## Data Preprocessing and Cleaning 

The aforementioned raw data set was found to contain the following flaws: 

- **Missing values in the *YearsWithCurrManager* column**. Through exploratory data analysis, it is found that the number of years with the current manager is lowly associated with the employee’s attrition status. Given that it contains missing values too, the *YearsWithCurrManager* column will be excluded from data analysis. 

- **Duplicate rows in the data set**. The raw data set contains 1,480 rows of employee data, out of which 10 are duplicated across all columns, or all columns except the *YearsWithCurrManager* column. The *EmpID* column values are used as unique identifiers for each employee represented in the data set, and only one row per unique *EmpID* is kept in the data set. 

- **Inconsistent categorical data labeling**. The categorical *BusinessTravel* column contains the values *TravelRarely* and *Travel_Rarely* — both refer to the same group of employees who rarely travel for business but have formatting discrepancies. To avoid confusion, the two categories are collapsed under the majority *Travel_Rarely* category. 

The above data cleaning steps were performed in Microsoft Excel. After data cleaning, the data set has 38 columns and 1,470 rows. The cleaned data set can be found in the *Cleaned Data Set* worksheet of the `HR_Analytics_Cleaned.xlsx` file attached. 

The `HR_Analytics_Cleaned.xlsx` file also contains three other worksheets: *Rounded Donut Chart Non-Travel*, *Rounded Donut Chart Travel Freq* and *Rounded Donut Chart Travel Rare*. These are dummy data sets created to build the Attrition Rate by Business Travel visualisation. For a detailed breakdown on the construction of this visual, refer to [this](https://tableau.toanhoang.com/tableau-qt-rounded-doughnut-chart/) online tutorial. 

The attached `Waffle Chart Template.xlsx` file is a dummy [data set](https://onedrive.live.com/:x:/g/personal/43EBDBC5D5265516/s!AhZVJtXF2-tD1UllBtCnb9YaZkvc?resid=43EBDBC5D5265516!10953&ithint=file%2Cxlsx&migratedtospo=true&redeem=aHR0cHM6Ly8xZHJ2Lm1zL3gvcyFBaFpWSnRYRjItdEQxVWxsQnRDbmI5WWFaa3Zj) to build the Attrition Rate waffle chart, provided by courtesy of [Andy Kriebel](https://www.vizwiz.com/2017/01/tableau-tip-tuesday-how-to-create.html). In addition to this resource, [this](https://www.youtube.com/watch?v=kR9f691FczI) online tutorial was referenced during the creation of the visual. 

## Post-Project Insights

- The attrition rate appears to be highest among younger workers aged 18-25 years old. 

- It appears that attrited workers are those who have to travel more for work. On average, attrited workers report a greater distance from home, and have to travel longer distances to get to work. Furthermore, the attrition rate seems to be higher when the number of business travels increases. Attrition rate is lowest among workers who do not have business travels, and is the highest among workers who have frequent business travels. 

- The education fields with the highest attrition rates are Human Resources, Technical Degree, Marketing. 

- The Human Resources and Sales departments have higher attrition rates. Across all 3 departments, it appears that lower-ranking job roles like Human Resources, Laboratory Technician and Sales Representative have higher attrition rates as compared to managerial roles. 

- Singles have a significantly higher attrition rate as compared to other marital status categories.  In particular, single males report a considerably high attrition rate.

- It appears that attrited workers tend to earn lower salaries than their active counterparts. The median daily rate and monthly income of attrited workers is significantly lower than that of active workers, as well as the overall median daily rate and monthly income. 

- It appears that attrited workers are those who tend to be less experienced at work. The median years worked in the company and total working years for attrited workers is lower than that for the active workers.
