# Apache Superset Setup Example

##Prerequisites for running the Example 

Ensure that Superset is installed along with the appropriate Python libraries such as Flask and PyHive, and an admin user and password has been set up, as well as having the server up and running.





## Adding the Presto Database 


Click on **Databases**  under the **Data** tab

Click the **+** sign and you will see a form to add a new database.

![Adding Database](resources/adding_database.png)


Give the database a name and set the SQLAlchemy URI of the form:

`presto://prestouseremail:prestopassword@prestourl:8446/geospock`

 * prestouseremail is an email account that has access to the database.
 * prestopassword is the password associated to the email account.
 * prestourl is the database url of the form `sqlaccess.'deploymentname'.db.geospock.com`



In the extras section, provide the following parameters:
```json
{
    "metadata_params": {},
    "engine_params": {"connect_args": {"protocol": "https"}},
    "metadata_cache_timeout": {},
    "schemas_allowed_for_csv_upload": []
}
```

Specifying the https protocol within the connect_args passed to `engine_params` ensures https is enabled.

Click on **Test Connection** and you should get an ‘ok’ notification.

By default, Superset takes the latest version of presto but this can be changed to 
an older version in the extra parameters when configuring the database by adding the following:

E.g.
```json
{
       "version": "0.123"
   }
```


## Getting Data  --> Extracting whole tables

To retrieve a full dataset (only recommended for small datasets), click the **+** sign under **Datasets**. 
Provide the database name, schema and dataset table name (in this example shown, tweet is the dataset).

![Data](resources/data.png)



## Creating Queries  --> Extracting data through queries
  

To create a new custom query, select **SQL Lab** and **SQL Editor**.

Write the query and save it. The query will then be available in the list of queries.  

To explore the data in a chart, click the explore button after the query has been run. 


![Custom query](resources/custom_query.png)


This will show the data in a table but this can be changed by changing the visualization type.



## Dataset access and Dashboard creation 

To create a visualisation on a full dataset, click the **+** sign under **Charts** and select the data source and visualization type.  

Ensure the correct columns are referenced in the right sections on the UI to display the data. 
You can also do UI filters, **GROUP BY** on columns and **LIMIT** on the number of rows as well if you wish.


With custom queries, to get to the chart view, click on **Explore**. By default, the chart will be a table but this can be changed. 


When you save a chart you get given an option to either save to a new dashboard or to an existing dashboard.

![Paris data](resources/Paris_data.png)





More example charts can be found on this link: 
https://superset.apache.org/docs/creating-charts-dashboards/first-dashboard
