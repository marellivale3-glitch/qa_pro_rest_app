\# JMeter API Load Testing



\## Project Description

Performance testing of a local REST API using Apache JMeter 5.6.3.



\## Environment

\- OS: Windows 11

\- Java: OpenJDK 21

\- JMeter: 5.6.3

\- Backend: Node.js

\- Base URL: http://localhost:3001



\## API Endpoints

1\. POST /character

2\. GET /characters

3\. GET /character/{id}

4\. PUT /character/{id}

5\. DELETE /character/{id}



Random character names are generated using JMeter functions.



Character IDs are extracted from POST responses using JSON Extractor.



\## Load Testing Results



| Users | Ramp-up | Loops | Requests | Errors |

|-------|---------|-------|----------|--------|

| 100 | 1 sec | 1 | 500 | 0% |

| 1000 | 1 sec | 2 | 10000 | 41% |

| 5000 | 1 sec | 4 | 100000 | 66.75% |



\## Duration Assertion



Duration Assertion threshold: 1000 ms.



The updated test plan was validated with one user.



Extended high-load tests were not executed due to local

hardware limitations and instructor permission.



\## Reports



\- report\_100

\- report\_1000

\- report\_5000



Each report contains an HTML dashboard (index.html).



Original JTL results are also included.



\## Conclusions



The API handled the initial test with 100 users without errors.



At higher loads, significant connection failures occurred.



Most failures were caused by refused connections to localhost:3001.



The original reports were generated before improvements

to dynamic character ID handling.



\## Recommendations



\- Investigate server connection limits.

\- Improve application stability under high concurrency.

\- Optimize character ID management.

\- Repeat high-load testing in a suitable environment.

