# \# JMeter API Load Testing

# 

# \## Project Description

# Performance testing of a local REST API using Apache JMeter 5.6.3.

# 

# \## Environment

# \- OS: Windows 11

# \- Java: OpenJDK 21

# \- Apache JMeter: 5.6.3

# \- Backend: Node.js

# \- Base URL: http://localhost:3001

# 

# \## API Endpoints

# 1\. POST /character - Create a character

# 2\. GET /characters - Get all characters

# 3\. GET /character/{id} - Get character by ID

# 4\. PUT /character/{id} - Update character

# 5\. DELETE /character/{id} - Delete character

# 

# Character names are generated randomly.

# Character IDs are extracted from POST responses using JSON Extractor.

# 

# \## Test Results

# 

# | Users | Ramp-up | Loops | Requests | Error Rate |

# |-------|---------|-------|----------|------------|

# | 100 | 1 sec | 1 | 500 | 0% |

# | 1000 | 1 sec | 2 | 10000 | 41% |

# | 5000 | 1 sec | 4 | 100000 | 66.75% |

# 

# \## Duration Assertion

# Duration Assertion is configured with a threshold of 1000 ms.

# 

# The updated test plan was successfully validated with 1 user.

# 

# Extended duration tests were not executed due to local hardware limitations and instructor permission to skip heavy tests.

# 

# \## HTML Reports

# \- report\_100

# \- report\_1000

# \- report\_5000

# 

# Each report contains an index.html dashboard.

# 

# \## Conclusions

# 

# The API successfully handled 100 concurrent users without errors.

# 

# At 1000 and 5000 users, the error rate increased significantly.

# 

# Most failures were connection refused errors, indicating that the local server could not accept all incoming connections.

# 

# The original load reports were generated before improvements to dynamic character ID handling.

# 

# The updated JMeter test plan uses dynamic IDs and includes Duration Assertion.

# 

# \## Recommendations

# \- Improve server stability under high concurrency.

# \- Investigate connection refused errors.

# \- Optimize character ID management.

# \- Repeat performance testing in a more powerful environment.

