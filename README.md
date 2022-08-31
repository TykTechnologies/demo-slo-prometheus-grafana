# SLIs and SLOs with Prometheus and Grafana for your APIs

## About

This is a demo project running on Docker, that shows how to configure [Tyk Gateway](https://github.com/TykTechnologies/tyk), [Tyk Pump](https://github.com/TykTechnologies/tyk-pump), Prometheus and Grafana to set-up a dashboard with SLIs and SLOs for your APIs managed by Tyk.

You can use it to explore the Prometheus metrics exposed by Tyk Pump and use them to set-up SLIs and SLOs in Grafana.

![SLOs-for-APIs-managed-by-Tyk-Dashboards-Grafana](https://user-images.githubusercontent.com/17831497/187458994-a8bc0eae-e9b6-4af5-9233-034dc981bae6.png)

  
## Deploy and run the demo

1. Clone this repository:

```
git clone https://github.com/TykTechnologies/demo-slo-prometheus-grafana.git
```

2. Start the services

```
cd ./demo-slo-prometheus-grafana/
docker compose up -d
```

3. Verify that all services are running

- Tyk Gateway
    - Health check runs on [http://localhost:8080/hello](http://localhost:8080/hello)
    - httpbin API runs on [http://localhost:8080/httpbin/](http://localhost:8080/httpbin/)
    - httpstatus API runs on [http://localhost:8080/status/](http://localhost:8080/status/)
- Tyk Pump
    - Health check runs on [http://localhost:8083/health](http://localhost:8083/health)
    - Prometheus metrics endpoint runs on [http://localhost:8084/metrics](http://localhost:8084/metrics)
- Prometheus runs on [http://localhost:9090/](http://localhost:9090/)
- Grafana OSS runs on [http://localhost:3000/](http://localhost:3000/)
    - The default log-in at start is admin/admin, once logged in you will be prompted for a new password

4. Generate traffic

K6 is used to generate traffic to the API endpoints. The load script [load.js](./deployments/k6/load.js) will run for 15 minutes.

```
 docker compose run  k6 run /scripts/load.js
```

You will see K6 output in your terminal:

<img width="963" alt="K6" src="https://user-images.githubusercontent.com/17831497/187454878-c1182107-7de2-4cd0-b572-9bcc80dde6c3.png">


5. Check out the dashboard in Grafana

Go to [Grafana](http://localhost:3000/) in your browser (initial user/pwd: admin/admin) and open the dashboard called *SLOs for APIs managed by Tyk*.

You should see the data coming in:
![tyk_grafana_initial](https://user-images.githubusercontent.com/17831497/187455646-077ac8a2-8279-4c23-8ca2-d276c0b2180b.png)

You can also filter the data per API:

<img width="472" alt="tyk_grafana_select_api" src="https://user-images.githubusercontent.com/17831497/187456007-e989119e-053a-4ff7-bc3a-5afd92482d5b.png">


## Tear down

Stop the services

```
docker compose stop
```

Remove the services

```
docker compose down
```

## How this works

TODO: work in progress

### Tyk Gateway

### Tyk Pump

### Prometheus

todo: add details about the query

Example definition inspired from: https://sre.google/workbook/slo-document/. See also https://sre.google/workbook/implementing-slos/#what-to-measure-using-slis and https://sre.google/workbook/alerting-on-slos/ to learn more about SLIs and SLOs.


__SLI: the proportion of successful requests, as measured from Tyk API Gateway__

* Any HTTP status other than 500–599 is considered successful.
* count of "api" http_requests which do not have a 5XX status code divided by count of all "api" http_requests
* SLO: 95% successful requests

### Grafana





## PRs
Explain the requirements for a PR...
  
#### SLA
First response (clarifying questions/guidance on improvements/answering questions) - target of 48 hours
Detailed review and feedback on PRs - target 7 days
  
  
  
## Bugs

#### SLA
First response (clarifying questions/guidance on improvements/answering questions) - target of 48 hours
  
  
  
## Features
  
#### SLA
First response (clarifying questions/guidance on improvements/answering questions) - target 72 hours
  
### Questions
For question on products, please use [Tyk Community forum](https://community.tyk.io/).
  <br>
Clients can also use support@tyk.io.
   <br>
Potential clients and evaluators, please use info@tyk.io.

  
