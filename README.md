# Grafana-InfinityDashboard
#### Simple dashboard for QA/Regression result representation and trend analysis

Grafana dashboard with infinity plugin

Visualize data from JSON, CSV, XML, GraphQL, HTML & REST APIs. Also turns any website into grafana dashboard.

Reference: https://sriramajeyam.com/grafana-infinity-datasource/ <br>
Sample Dashboard: https://safehouseinn.grafana.net/goto/yKNYU9H4z?orgId=1
<br>

The idea is to have a dashboard for viewing test results of regression run

### Approach: <br>
Get the test results in CSV/Json format. Put the result file in any place where the same can be retrieved/accessed by HTTP method or over URL. (Here used git itself, the provided dashboard reads the data from the [sample.csv](sample.csv) file in root).
Use UQL in case of json, or in case of csv use the configure columns to process the retrieved data. 

All the panels/monitors in the displayed dashboard are created using only the data available in the csv file through different grafana transformations. Once data is available in table format, which the plugin does, rest of the dashboard/widgets can be created through grafana transformations itself.


Sample Dashboard:  <img src="resources/grafana-dashboard-snap.png?raw=true">

Working Model:<img src="resources/GrafanaDashModel.gif">
