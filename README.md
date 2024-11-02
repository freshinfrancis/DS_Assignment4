# DS_Assignment4

##FailureHandlingTest
Description:
The FailureHandlingTest simulates a scenario where the server experiences unexpected disconnections. This test ensures that client applications can handle server failures gracefully and attempt reconnections or failovers as needed. It is designed to validate the reconnection logic and assess how well the system can recover from transient failures without losing data consistency.

What It Does:

Uploads initial data to the server to ensure a baseline of connectivity.
Simulates a server disconnection event.
Checks if clients can detect the failure, handle reconnection attempts, and resume normal operation without data corruption.
Best Use Case:
This test is ideal for systems requiring high availability and resilience, where unexpected server failures should not disrupt client functionality for long.

##ScalabilityTest
Description:
The ScalabilityTest assesses the system’s performance and stability under a high load of concurrent client requests. By simulating a growing number of client connections, this test measures how the server handles increased traffic and assesses performance metrics such as latency and throughput.

What It Does:

Starts with a minimal number of concurrent clients and incrementally increases the load.
Monitors response times, latency, and any connection failures as client count grows.
Logs metrics to analyze how well the system scales and maintains performance under load.
Best Use Case:
Useful for distributed systems that need to handle high volumes of concurrent users or data requests, providing insight into resource allocation and bottlenecks.

##FailureToleranceTest
Description:
The FailureToleranceTest focuses on fault tolerance by evaluating how effectively the system maintains data integrity and consistency during a server restart. This test simulates a server failure, restarts it, and checks whether clients can seamlessly reconnect and re-upload data if needed.

What It Does:

Initiates initial data uploads to verify successful connections.
Simulates a server failure by instructing a manual or automated server restart.
Checks if clients automatically reconnect and whether any lost data is successfully re-sent and consistent with the original data.
Best Use Case:
Ideal for applications where consistent data state is critical, even in case of planned or unplanned server downtime, such as financial or mission-critical systems.

##LamportClockOrderTest
Description:
The LamportClockOrderTest ensures that the distributed system maintains proper event ordering using Lamport clocks, a mechanism for logical ordering in distributed environments. This test validates whether the server correctly synchronizes Lamport clocks on client requests and maintains causally consistent ordering.

What It Does:

Launches multiple concurrent client instances that send requests with Lamport clock values.
Checks if the server updates its Lamport clock based on incoming requests and returns the correct clock value in responses.
Verifies that all events are processed in the correct causal order.
Best Use Case:
Useful for distributed systems where causally consistent ordering of events is critical, such as in collaborative applications or event-driven architectures.
