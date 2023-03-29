# influxdb-telegraf-grafana

This is an attempt of creating a lab using InfluxDB (1.8.10), Telegraf (1.19) and Grafana (latest). Telegraf collects the host hardware metrics and sends to InfluxDB. Visualization is done with Grafana. 

To run this lab make sure you have docker and docker-compose properly setup on your machine.

1. Run the command:

`docker-compose up`

2. On your browser open the address:

`http://localhost:3000`

This will open the grafana UI.

3. Click on “Add data source” to add an InfluxDB datasource:

![image](https://user-images.githubusercontent.com/123763719/228595418-83e862d4-a23b-46a6-af05-8d704ab778f9.png)

Next, select the InfluxDB option and click on “Select.”

Select the Basic Auth option, specify your administrator credentials, and fill the details about your InfluxDB database. Here is the final configuration:

<img width="756" alt="Screenshot 2023-03-29 at 16 52 01" src="https://user-images.githubusercontent.com/123763719/228595938-117f0c36-20d3-449b-a6a8-39ed36b041df.png">


<img width="1126" alt="Screenshot 2023-03-29 at 16 52 34" src="https://user-images.githubusercontent.com/123763719/228596123-de7b2a1b-32b5-4fa9-b7a4-15ecd89eb5d6.png">

Click on save and test.

4. Create a new dashboard by importing a preset

<img width="180" alt="Screenshot 2023-03-29 at 16 54 04" src="https://user-images.githubusercontent.com/123763719/228596538-a33bdd1b-4f86-4196-b224-ae2c92071e90.png">

In the import text box, put 1443 as a dashboard ID.

Now you should see your host metrics collected by Telegraf and ingested by InfluxDB being displayed by Grafana.

<img width="1240" alt="Screenshot 2023-03-29 at 16 55 40" src="https://user-images.githubusercontent.com/123763719/228596984-14d41355-f41b-44c8-a316-e41a2845d178.png">

