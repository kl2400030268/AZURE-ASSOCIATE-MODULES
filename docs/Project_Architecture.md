# Project Architecture

## System Architecture

The proposed system consists of a React frontend, Spring Boot REST API,
MySQL database, external API/service, OpenTelemetry instrumentation,
and Azure Application Insights.

```text
                         ┌──────────────┐
                         │     User     │
                         └──────┬───────┘
                                │
                                ▼
                       ┌─────────────────┐
                       │ React Frontend  │
                       └────────┬────────┘
                                │
                                ▼
                       ┌─────────────────┐
                       │ Spring Boot     │
                       │ REST API        │
                       └───────┬─────────┘
                               │
                    ┌──────────┴──────────┐
                    │                     │
                    ▼                     ▼
             ┌─────────────┐       ┌──────────────┐
             │    MySQL    │       │ External API │
             │  Database   │       │   Service    │
             └─────────────┘       └──────────────┘
                    │                     │
                    └──────────┬──────────┘
                               ▼
                       ┌─────────────────┐
                       │  OpenTelemetry  │
                       │ Instrumentation │
                       └────────┬────────┘
                                │
                                ▼
                  ┌──────────────────────────┐
                  │ Azure Application        │
                  │        Insights          │
                  └──────────────────────────┘




Component Description
React Frontend

Provides the user interface and communicates with the backend through REST APIs.

Spring Boot Backend

Provides REST APIs and handles the application's backend logic.

MySQL Database

Stores the application's business and application data.

External API

Represents an external service dependency used by the backend.

OpenTelemetry

Acts as the instrumentation layer for collecting application telemetry.

Azure Application Insights

Collects and analyzes telemetry such as requests, dependencies, exceptions, traces, metrics, and application component relationships.

Monitoring Flow

User → React Frontend → Spring Boot REST API → Database / External API → OpenTelemetry → Azure Application Insights


