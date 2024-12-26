
## Chapter 6 - Creating Workbench Reports


## Chapter 6  Creating Workbench Reports

 
1. Introduction to Workbench Reports
2. Creating Workbench Reports
    - Reporting Workbench Templates
    - Reporting Workbench Reports
        - General Tab
        - Criteria Tab
        - Display Tab
3. Reporting Workbench Results
4. Reporting Workbench Links on a Dashboard
5. Exercise 6 1: Create a Workbench Report
6. Exercise 6 2: If you have time ... Create a Report Listing Component
7. Visualizing Workbench Results
8. Workbench Visualizations
9. Workbench Summaries
10. Graph and Table Components
11. Exercise 6 3: Creating a Workbench Summary and Adding it to a Dashboard
12. Exercise 6 4: If you have time ... Add a Visualization from the Explore
tab to a Dashboard
13. Exercise 6 5: If you have time ... Enable Parameters for your Summary


 
##  Introduction to Workbench Reports  
 
Some report requests require real time data and a greater level of flexibility and customization. 

Cogitos **Reporting Workbench tool** that can query Chronicles directly as well as Clarity 
and Caboodle. Which database is queried depends on the **configuration settings** in the 
**Workbench template**.

By the End of This Lesson, You Will Be Able To...
1. Find available Workbench reports and templates in the Analytics Catalog
2. Run Workbench reports and view their results
3. Use the Explore tab to visualize report results
4. Create and modify Workbench reports
5. Distribute Workbench content on a dashboard



## Creating Workbench Reports 6 2

The Reporting Workbench framework consists of records in the following **master files**:

1. **HGR**  **template records** define the search, criteria, and display options
2. **HRX**  **report records** define which criteria, values, and display options will be used
3. **HRN**  **run records** are generated each time a report is run
4. **HGV**  **visualization records** are graphs saved while viewing the results

Epic released Workbench reports and templates have entries in the **Report Repository**.



## Reporting Workbench Templates   page 165   6.2a

The **template** determines what search engine the report will use: 
1. Ad Hoc
2. SQL
3. Code template.

Templates that use an **Ad Hoc** or **Code template** search engine can search **Chronicles data**. Templates that
use a **SQL** search engine begin their search in **Clarity** or **Caboodle**, with the ability to query additional data
points drawn from Chronicles.

#### Create a Workbench Report from a Template  page 165
 
1. Log in to Hyperspace as Lorena.
2. Open the Analytics Catalog.
3. Search for the Find Patients   Generic Criteria [17500] template.
4. Double click the template to create a new report.



## Reporting Workbench Templates 

Each Workbench report is created from a **template**. All reports from the same template share key
characteristics:
- The **result granularity**, or the meaning of one row, is defined by the **Workbench template**.
- For **Chronicles based Workbench templates**, the result granularity will either be records or
contacts from a Chronicles master file. The **Search Master File** and **Search On fields** of the
template define the **granularity**.
- The **data source**, or the database from which Workbench retrieves its result set, is defined by
the **Search Engine** setting in the Workbench template.
- **Templates** that retrieve only **Chronicles data** will use the **Ad Hoc** search engine or a
specialized, **code based** search engine.
- **Templates** that retrieve data from **Clarity or Caboodle** use a **SQL search engine** to generate a
list of results. 

These templates can optionally use the Ad Hoc search engine to refine the results based on Chronicles
data.

**Workbench templates** can be found in the **Analytics Catalog** and can be differentiated from reports by
their icon.


