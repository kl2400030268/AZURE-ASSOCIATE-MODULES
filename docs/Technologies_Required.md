# Services / Technologies Required

The following technologies and services are required for the development,
instrumentation, testing, and monitoring of the web application.

| S.No. | Technology / Service | Purpose |
|------:|----------------------|---------|
| 1 | React | Used to develop the frontend/web interface. |
| 2 | Spring Boot | Used to develop the backend REST APIs and application logic. |
| 3 | MySQL | Used to store and manage application data. |
| 4 | Spring Security | Used for authentication and authorization. |
| 5 | JWT | Used for secure authentication and protected API requests. |
| 6 | OpenTelemetry | Used as the instrumentation layer for collecting application telemetry. |
| 7 | Azure Application Insights | Used for application monitoring, performance analysis, dependency tracking, and error monitoring. |
| 8 | Postman | Used to test and verify REST APIs. |
| 9 | External API / Service | Used as an external dependency for monitoring and performance analysis. |

## Main Monitoring Features

Azure Application Insights will be used to monitor:

- Requests and API response duration
- Database and HTTP dependencies
- Application exceptions and failures
- Diagnostic traces
- Application performance metrics
- Application component relationships using Application Map
- Telemetry using Kusto Query Language (KQL)
- Alerts based on selected performance or failure conditions