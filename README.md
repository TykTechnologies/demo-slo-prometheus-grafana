# SLOs for your APIs with Tyk, Prometheus and Grafana
<!-- Tell other people why your project is useful, what they can do with your project, and how they can use it.
As explained in GitHub it typically includes information on:
1. What the project does
2. Why the project is useful
3. How users can get started with the project
4. Where users can get help with your project
5. Who maintains and contributes to the project
For more details check GitHub [doc](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)

PLEASE CHANGE THIS FILE NAME TO BE "README.md" so GitHub can automatically surface it to repository visitors.
-->

## About

This is a demo project, using an OSS deployment of Tyk Gateway, Tyk Pump, Prometheus, Grafana and K6 running on Docker. 
  
## Purpose

You can use it to explore the Prometheus metrics exposed by Tyk Pump in Grafana, to set-up SLIs and SLOs. 
  
## Deploy and run the demo

1. Clone this repository:

```
git clone https://github.com/TykTechnologies/demo-slo-prometheus-grafana.git
```

2. Start the services

```
docker compose up -d
```

3. Verify that all services are running

- [Tyk Gateway](https://github.com/TykTechnologies/tyk)
    - Health check runs on [http://localhost:8080/hello](http://localhost:8080/hello)
    - httpbin API runs on [http://localhost:8080/httpbin/](http://localhost:8080/httpbin/)
    - httpstatus API runs on [http://localhost:8080/users/](http://localhost:8080/users/)
- [Tyk Pump](https://github.com/TykTechnologies/tyk-pump)
    - Health check runs on [http://localhost:8083/health](http://localhost:8083/health)
    - Prometheus metrics endpoint runs on [http://localhost:8084/metrics](http://localhost:8084/metrics)
- Prometheus runs on [http://localhost:9090/](http://localhost:9090/)
- Grafana OSS runs on [http://localhost:3000/](http://localhost:3000/)
    - The default log-in at start is admin/admin, once logged in you will be prompted for a new password

4. Generate traffic

K6 is used to generate traffic to the API endpoints
The load script [load.js](./deployments/k6/load.js) will run for 15 minutes.

```
 docker compose run  k6 run /scripts/load.js
```

5. Check out the dashboard in Grafana



## Tear down

Stop the services

```
docker compose stop
```

Remove the services

```
docker compose down
```

## SLIs and SLOs


## Grafana


Go to [Grafana](http://localhost:3000/) in your browser and open the dashboard called *SLOs for APIs managed by Tyk*.

## SLIs and SLOs

Example definition inspired from: https://sre.google/workbook/slo-document/. See also https://sre.google/workbook/implementing-slos/#what-to-measure-using-slis and https://sre.google/workbook/alerting-on-slos/ to learn more about SLIs and SLOs.


__SLI: the proportion of successful requests, as measured from Tyk API Gateway__

* Any HTTP status other than 500–599 is considered successful.
* count of "api" http_requests which do not have a 5XX status code divided by count of all "api" http_requests

__SLO__

* 95% successful requests


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

  
