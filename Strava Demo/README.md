# Strava Reporting
Here are the resources to replicate the demos I include in blog posts and videos and have demo'd at multiple events. 
## Power BI Report
In this repo I have a Power BI report template. It needs a SharePoint library and a SQL Server table. 
* [Power BI Template]()
* [SQL to build table]()

## Data Flow using Power Automate
* When I record exercise in Strava that creates an activity.
* I download that activity as a tcx file into a SharePoint library called Landed
* A Power Automate flow picks up the tcx file, removes all references to Garmin schemas and saves it as an XML file in a SharePoint library called Cleaned (No video yet but it's coming)
* When a new file arrives in Cleaned a flow triggers to refresh my report
    * Blog post - [Power Automate Write me a flow](https://hatfullofdata.blog/power-automate-write-me-a-flow/)
    * Power BI report - see above
* On a schedule a flow pulls data out of the Power BI and sends the data in an email to the coach
    * Blog post - [Power Automate - Get data from a Power BI dataset](https://hatfullofdata.blog/power-automate-get-data-from-a-power-bi-dataset/)
* The report includes charts with highlighted sections for the different sections of my exercising, eg Warm Up, Interval etc. This is calculated using the Activity Sections table.When viewing the report on the Add Sections page, I can click on point on the chart, select a section name and click the flow button to add a row to the table to annotate my data.
    * Blog post - [Power Automate button in a Power BI Report](https://hatfullofdata.blog/power-automate-button-in-a-power-bi-report/)