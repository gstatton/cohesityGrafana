# cohesityGrafana

Grafana allows you to query, visualize, alert on and understand your metrics no matter where they are stored. Create, explore, and share dashboards with your team and foster a data driven culture. With Grafana running on Cohesity, you can connect it directly to the Custom Reporting Database to execute time-series queries to visualize your backup data over customized periods of time.


In order to connect Grafana to the Cohesity Custom Reporting Database, first you must generate the login credentials and connection information:

log in via iris_cli and execute:
custom-reporting db

From the output returned, grab the Host IP, Port, Username, Password for Grafana


Create a new data source in Grafana that is of type Postgres, the input the information from the output (from the link above).



Once a db connection is established with Grafana, you can import this template to get you started on building time-series queries and panels in Grafana!
