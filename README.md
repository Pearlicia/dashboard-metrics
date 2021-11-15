**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

*TODO:* run `kubectl` command to show the running pods and services for the three components. Copy and paste the output or take a screenshot of the output and include it here to verify the installation

Done: Pods and Services - (answer-img/pods-and-services.png)


## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.

Done: Grafana Dashboard - (answer-img/grafana-homepage.png)

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
Done: Basic Dashboard - (answer-img/basic-dashboard.png)

## Describe SLO/SLI
*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.

DONE: Since a Service-Level Indicator (SLI) is a specific metric used to measure the performance of a service.
The SLIs based on an SLO of monthly uptime and request response time are the actual measurement of the SLOs like the SLIs indicate the level of performance the service actually exhibited and show whether the SLO was achieved or not.


## Creating SLI metrics.
*TODO:* It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 

Done:
* Latency - The time taken to serve a request (usually measured in ms).
* Traffic - The amount of stress on a system from demand (such as the number of HTTP requests/second).
* Errors - The number of requests that are failing (such as number of HTTP 500 responses).
* Saturation - The overall capacity of a service (such as the percentage of memory or CPU used).
* Network Capacity - The average bandwidth


## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.
Done:
Service Uptime- (answer-img/service-uptime.png)
Error 40x-(answer-img/b-f-error404.png)
Error 50x-(answer-img/error500.png)


## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here.
Done: Jaeger Span - (answer-img/jaeger-span.png)


## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.
Done:
Jaeger dashboard metric - (answer-img/jaeger-in-dashboard.png)


## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue.

Done:
TROUBLE TICKET

Name: Trial app error

Date: 11-15-2021

Subject: Internal Server Error


Affected Area: The trial app

Severity: High

Description: The error message reads: "The server encountered an internal error and was unable to complete your request. Either the server is overloaded or there is an error in the application."


## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name three SLIs that you would use to measure the success of this SLO.

Done:
* Service uptime is greater than 99.95%
* HTTP status code returns 20X for more than 99.95% of requests
* HTTP request average response time is less than 100ms.
* Memory and CPU usage is Moderate


## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create KPIs to accurately measure these metrics. We will make a dashboard for this, but first write them down here.
Done:
Uptime -
    The amount of time for an application to be running.
    It is very important to have an application to have an uptime greater than 95%, so that user will not face problem
    It includes the uptime of Front-end, Back-end and Trial uptime
Latency -
    The time it takes for a request to be served by an application, often measured in millisecond
    It is very important to keep track of successful and fail(error) response to requests
Error rate -
    Number of HTTP error caused by application to total number of HTTP response
    It is important to ensure the application has an error budget of less than 1%
CPU and Memory usage -
    The amount of CPU and Memory used by the application
    It is important to ensure CPU or Memory usage is not more than 75%, otherwise it can have bad impact on the application


## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  

Done:
Service Uptime - (answer-img/service-uptime.png) - Displays both the frontend and backend service uptime
Error rate - (answer-img/b-f-error404.png) Displays the backend and frontend errors
Backend memory and CPU usage - (answer-img/backend-cpu-usage.png answer-img/backend-m-usage.png
Frontend memory and CPU usage - (answer-img/front-cpu-usage.png answer-img/frontend-m-usage.png
Trial app cpu usage - (answer-img/trial-cpu-usage.png)