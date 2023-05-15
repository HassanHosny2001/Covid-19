#Automated COVID Dataset Pipeline Workflow

#Data Ingestion:
- Create a folder named "/home/cloudera/covid_project" on the virtual machine.
- Inside the "covid_project" folder, create two subfolders: "landing_zone" and "scripts".
- Use WinSCP to upload the dataset "covid-19.csv" into the "landing_zone" folder ("/home/cloudera/covid_project/landing_zone/COVID_SRC_LZ").

#Data Loading:
- Load the dataset from "COVID_SRC_LZ" to HDFS directory named "/user/cloudera/ds/COVID_HDFS_LZ" using HDFS command line interface (CLI) commands in a shell script.

#Hive Database Setup:
- Create a database in Hive.
- Create the following schemas in Hive:
** 1st Hive staging table for pointing to the dataset location to select data from.
** 2nd Hive ORC table partitioned by Country to improve query performance.
** 3rd Final Hive table to generate the report and output file for visualization.

#Oozie Workflow Setup:
- Use Cloudera HUE on the virtual machine to create an Oozie workflow.

Execute Oozie Workflow:
- Manually run the Oozie workflow job from HUE to process the data and generate the final output.
- The final output file will be located at "/user/cloudera/ds/COVID_FINAL_OUTPUT" in HDFS.

Data Visualization:
- Download the final output report file from the HDFS file location mentioned above.
- Visualize the downloaded file using Power BI, applying filters for each visualization requirement (top 10 ranking countries in death rate, top 10 ranking countries in testing rate, and top 10 ranking countries in testing rate on a pie chart).
