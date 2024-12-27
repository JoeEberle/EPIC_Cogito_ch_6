
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




## Reporting Workbench Reports

Just as every **SlicerDicer session** is built from an **existing data model**, every **Workbench report** is built
from an existing **template**. 

A **Workbench report** can query **Chronicles, Clarity, or Caboodle** depending on
the template used to build the report. 



## Reporting Workbench Reports 

Just as every **SlicerDicer session** is built from an **existing data model**, every **Workbench report** is built
from an existing **template**. 

A **Workbench report** can query **Chronicles, Clarity, or Caboodle** depending on
the template used to build the report. 

The **template** also defines what **criteria**, **display columns**, and **actions** can be taken on the report.

To **modify an existing report**, click the **pencil icon** for the report from the **Analytics Catalog.**

You can also right click and select Edit.

# 

## The following **Report Settings tabs** form the basis of report build:

#### Criteria tab 

**Criteria tab** This tab is used to set the criteria, date range, and logic. It determines which rows
will be returned by the report when it is run. With the appropriate security,
administrators can add additional criteria that are not available from the
template.

Date range behavior varies by template. See the Criteria Tab section for more
information.

#### Display Tab

**Display tab** This tab is used to **add or remove display columns** from the report and to add
detailed views to the results. With the appropriate security, administrators can add
**additional columns** that are not available from the template.

Each display column is a PAF record. Its job is to retrieve data and display it on a
report.

#### Summary tab

**Summary tab** This tab is optional and used to **visualize aggregated data** about report results.




## Criteria Tab

The **criteria tab** controls the search. When creating a new report from a template, some criteria 
may be selected automatically. These default criteria are set by the template. Additional criteria may be selected by using the search bar at the top of the Report Settings window.
Search by keyword and press ENTER or click the magnifying glass to browse the full list.

Some administrators will have the security to **add additional criteria** to the list using the **Add
Criterion** button at the bottom of this list of criteria. Using this option well typically requires
knowledge of the Chronicles database and additional training on Workbench template settings.



## Report Logic and Criterion Logic

The **default report logic** will be **AND logic**, meaning that all criteria must be met for a row to be returned
in the results. Click the AND button to toggle to the OR and CUSTOM options. Custom logic assigns a
number to each criteria, which can then be referenced with a logical expression.

Most **criteria** use **OR logic** by default. Criterion logic can also be toggled by clicking 
the button until the OR or CUSTOM option appears.

For a similar discussion of logic options in SlicerDicer, see the **Criteria section** of the 
SlicerDicer Populations chapter.



## Date Range

There are several ways to evaluate dates in Reporting Workbench. Which options are available depends
on the Workbench template settings and the master file being searched.

## Default Date Range Behavior
The Workbench ad hoc search engine evaluates criteria as it works through the Chronicles hierarchy.
1. **Master file** the Workbench template has one search master file.
2. **Records** the search engine identifies records to include in the search results. It evaluates recordlevel
criteria  to determine which records to include.
3. **Contacts** the search engine identifies which contacts to include in the search results. It evaluates
overtime criteria to determine which contacts to include.

The date range found at the top of the **Report Settings window** is used to evaluate time sensitive,
or **overtime criteria**. **Overtime criteria** can be identified by the clock icon on the Criteria tab.

If a Workbench report using the default date range behavior does not include any overtime criteria, the
date range will not be used.



## Specialized Date Range Behavior

Some Workbench templates apply custom date range behavior using specialized M code. For example,
the Find Orders [440] template can apply the date range to Order Creation Date, Medication
Administration Date, or other dates related to orders. This is similar to the Dates card behaviors present in
most SlicerDicer data models.




## Date Criteria

Some items in Chronicles store dates. It is possible to add Workbench criteria to evaluate these dates. For
example, the Enrollment Date is an item in the **Episodes (HSB) master file**. A Workbench report could
apply a criteria evaluating this item to find all episodes with an enrollment date in the last two weeks.

Recall that the template defines what criteria will be available, and therefore what dates can be evaluated
as criteria on a given report.

For a similar discussion of date options in SlicerDicer, see the Criteria: Advanced Options section of the
**SlicerDicer Populations** chapter.

**When building a new report**, it is common to test the report by **re running** it. Reporting
Workbench will rerun a report if there have been any changes to the Criteria, Display, or
Summary tab, regardless of the Hours to keep results setting. It’s also possible to run a Trace
to force a report to re run. The Trace feature is covered in the Troubleshooting lesson.

**HRN records** can be saved and even customized by the consumer, but they are ultimately temporary: all
HRN records eventually get purged from the system a few months after they expire.



## View Manager

Users can click the **View Manager** to save a view (filters and sorting on the Detail List﴿ or save a
Workbench visualization ﴾a graph built in the Explore tab).

