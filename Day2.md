# Day 02 
## ELK Stack Introduction 
### What does ELK mean :- <br>
- E in ELK stands for Elasticsearch
- L in ELK stands for Logstash
- K in ELK stands for Kibana

#### Elasticsearch 
Its a database that is used to store Windows event logs, Syslogs, firewall logs and almost anything. It also has the capability to search accross the data. It uses a query language called ES|QL (Elastic Search Query Language), it also uses RESTful APIs and JSON because of which we can use different applications to interact with the elastic search database in a programable way to get the required information.
#### Logstash 
Logstash is a free and open serve side data processing pipeline that collects telegemtry from various souces and it also transforms, filters and opens it into the elasticsearch instance. 
<br>Two  of the many ways to collect telemetry is 
- Elastic Agents which can collect all different types of data using one unified agent per host.
- Beats - there are 6 different types of beats -<br>
          - File beat for Logs<br>
          - Metric Beat for Metric<br>
          - Packet Beat for Network Data<br>
          - Winlog Beat for Windows Events<br>
          - Audit Beat for Audit Data<br>
          - Heartbeat for Uptime<br>
And the appropriate beats will be installed in the endpoint depending on the telemetry that has to be collected.<br>

When the logstash is configured then agents such as Windows machine will be able to forward their windows event logs into logstash using either Winlog beat or an elastic agent and then logstash will be able to transform those events and push it into the elasticsearch instance. Logstash has the capability to filter logs that meet a certain criteria making it costomizable to our environment.
#### Kibana 
Whem we use Kibana we have  
