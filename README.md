![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/c5e6e815-4608-43b3-a212-5688e709a0ab)



### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiOGZiYWMxODgtYjY0Ny00YmZkLWExZTktODM1ZTA0YzMyMzQ1IiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

## About

The main objective of building this dashboard is to conduct a thorough analysis of the business, focusing on customer base, revenue generation, growth rates policy changes, settlement and demographics. This aims to provide valuable insights for informed decision-making. This involves tracking key metrics and creating visual representations of daily trends over time. Filters are included for efficient analysis. based on various factors. This has separate pages for General Report, Sales-Mode and Age-Group will allow for in-depth understanding of their impact on the business.
In this project, we embark on a journey to gain a deeper understanding of our customer base and revenue generation at Shield Insurance. We prioritize tracking customer numbers and total revenue, while also closely monitoring daily growth rates for both. This real-time monitoring ensures we stay on course towards our goals.
I've tackled the following aspects:
- Understanding total number of customers company have and how much revenue they make.
- Keep an eye on how fast the revenue and customer numbers are growing each day.
- Looked at how the insurance policies changes from one month to another to spot trends and areas to improve.
- Grouping the customers by their age to see which cities and age groups make the most revenue and have the most customers.
- Used filters like sales methods, age groups, cities, months, and policy IDs to analyze our data faster.
- Separate page to study how different age groups impact the business - like what policies they prefer and how they settle claims.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv files.
![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/6d6d77ca-9244-49ae-853f-c61fb1e99a8c)

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : Correcting the datatypes of some columns and replacing incorrect names in some rows and columns.
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 6 : Since the data contains various ages, thus in order to represent age groups, a new calculated column was added using DAX called age groups.for creating new column following DAX expression was written;
        
        age_group = SWITCH(TRUE(),
            dim_customer[age] <= 24, "18-24",
            dim_customer[age] <= 30 , "25-30",
            dim_customer[age] <= 40, "31-40",
            dim_customer[age] <= 50, "41-50",
            dim_customer[age] <= 65, "51-65",
            "65 +") 

Snap of new calculated column ,

![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/8dc66b6a-69ba-4132-862e-665829cf6113)
- Step 7 : Visual filters (Slicers) were added for four fields named "Sales Mode", "Age Groups", "Cities", "Months" and "Policies".

   ![image](https://github.com/Ankit-KY/SHELD_INSURANCE/assets/148628279/abcfffe3-0dec-4209-8490-52d87264fa46)

- Step 8 : Four card visuals were added to the canvas, one representing total customers, second representing total revenue in millions, third representing Daily customer growth(DCG) & last one  representing Daily revenue growth(DRG).
           Using visual level filter from the filters pane, basic filtering was used.

Snap of General View KPI cards ,

![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/7890044e-0acc-4cdb-8445-1bb6ceeabcf8)
- Step 9 : Four card visuals were added to the canvas, one representing total customers, second representing total revenue in millions, third representing total offline sales in millions & last one  representing total online sales in millions.
           Using visual level filter from the filters pane, basic filtering was used.

Snap of Sales View KPI cards ,

![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/a2932e0c-53c5-49a9-ac50-9f9d50b77480)
- Step 10 : Three card visuals were added to the canvas, one representing total customers in thousands, second representing total offline customers & the last one  representing total online customers.
           Using visual level filter from the filters pane, basic filtering was used.

Snap of Age Segment View KPI cards ,

![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/fe4d2bee-6df7-42f7-93ec-bd6764daef62)
- Step 11 : A line chart was also added to the  general report design area representing the total customers by months. A button switch was also added above visual to switch to total revenue by months line chart.

Snap of Visual ,

![image](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/49f9b726-d750-4d8c-bb8f-d82a6b149e6c)
        
 - Step 12 : All the new measures were created for the analysis by using DAX expressions.
  
Snap of created measure.
 
![KPIs 1](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/346821cc-8f17-4480-8692-3f9fbf69dc59)

![KPIs 2](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/de9113e7-71c4-4c3d-bf24-6df4386e0194)

 - Step 13 : All the 3 dedicated pages were created for specific analysis,

  1. **GENERAL REPORT:** This general page comprises all aspects of revenue and customer data, including demographic information, sales mode, age group. It also includes analysis daily revenue / customer growth trend analysis and helps to find the policy wit highest revenue and customers.

![Shield Insurance General Page](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/cd0fa39a-1115-4944-bb89-4eb00d42a336)

  2. **SALES MODE:** This page is dedicated to various sales mode analyses for both customers and revenue. This page looks at how much money we are making and how many customers we have over a month. It also gives daily revenue for every sales mode.

![Shield Insurance Sales Page](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/5978be43-99b2-437c-b780-5ee4e9ed195e)


  3. **AGE SEGMENT:** This page focuses on various analysis related to the age groups of policy holders. It includes the number of policy holders in each policy, most preferred sales mode, policy wise revenue. Also, It helps finding average estimation for each group and identifies the customers with the highest estimated settlement.

![Shield Insurance Age Page](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/b743b7b3-1316-427d-b89e-2a782adc3ccf)

 - Step 14 : The report was then published to Power BI Service.

# Snapshot of Dashboard (Power BI Service)

![PowerBI Service](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/ee06f7d7-ed4a-4b7d-bd4a-61e5d3cff3f0)

 # Data Model Snapshot
 
![Data modelling Shield Insurance](https://github.com/Ankit-KY/AtliQ_Grands_Hospitality_Analysis/assets/148628279/5e512e67-6eca-495f-b9b7-f6e68b442650)

# Insights

A four pages report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

- The total revenue amounts to **989.25** millions, total customers counts to **26841**, alongside with a Daily Average Customer Growth  of 148(Approx)
- Date with Highest Revenue(16.79 M) and Highest Customers(418)  acquired is: **25 March 2023**
- Date with Lowest Revenue(2.05 M) and Customers (71) acquired is: **17 Nov 2022**
- Month with Highest Revenue(264 M) and Highest Customers(7081) acquired is: **March 2023**
- Month with lowest Revenue(131.7 M) and lowest Customers(3787) acquired is: **Nov 2022**
- City which Acquired Highest Total Revenue and acquired highest number of customers: **Delhi NCR**
- City which acquired lowest Total Revenue and acquired lowest number of customers: **Indore**
- Most preferred sales mode by Customers(55%): **Offline-Agent** whereas Least preferred sales mode(12%) : **Online-Website**
- Age Segment with highest Revenue and customer acquisition is: **31-40** whereas Age Segment with lowest Revenue acquisition is: **18-24**
- Age Segment with lowest Customer acquisition is: **65+**
- Policy with highest Revenue Acquisition (324M): **POL2005HEL**
- Policy with highest Customer Acquisition (4434): **POL4321HEL**
- ## Why old people buy costly policies ? 
  The data suggests that old people buy policies with costly premiums. Like, 577 senior citizens, which is a predominant headcount, buy POL2005HEL with premium of 120K. It’s because in old age most of the people came up with pre-existing diseases and are more likely to require frequent medical care, insurance companies usually charge a higher premium to cover them. 

  ### Recommendations
  So, it’s quite normal to say that most of the people don’t even buy the policies. To answer this problem, company can *analyze health risks in the 65+ age group and adjust premiums accordingly to accurately reflect potential claims costs*.

- ## Why march is the busiest month ?
  March is crucial in India's financial calendar, particularly for insurance purchases, driven by tax-saving motives. As the fiscal year ends, individuals rush to optimize tax liabilities, favoring insurance policies for their tax benefits. Strategic purchases, aided by tailored offerings and promotions, dominate this period. Additionally, the need for year-end tax declarations accelerates policy acquisitions. In essence, March represents a vital window for insurance investments in India. 

  ### Recommendations
  An insurance company can capitalize on other months also by
  -  Offering tax-saving insurance products.
  -   Providing incentives for March purchases.
  -  Training agents on tax-saving policies.
  - Utilizing digital channels for promotions.
  - Streamlining processes for efficiency.

#### Do you have  any questions ? Feel free to ask anything….
### Connect with me on [linkedin](https://www.linkedin.com/in/ankit-kumar-yadav3027)
