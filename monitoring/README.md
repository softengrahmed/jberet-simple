# Performance Metrics for Application Monitoring

This repository contains the suggested performance metrics for monitoring the application, along with a Grafana dashboard configuration.

## Metrics Suggested

1. **Job Execution Time**: Measures the time taken for a batch job to complete.
   - **Significance**: Identifies performance bottlenecks in batch processing.
   - **Source**: Derived from the `awaitTermination` method in the test.

2. **Job Completion Status**: Tracks the status of batch jobs (e.g., `COMPLETED`, `FAILED`).
   - **Significance**: Ensures jobs are completing successfully and helps identify failures.
   - **Source**: Derived from the `Assert.assertEquals` check for `BatchStatus`.

3. **Latency**: Measures the time taken to service a request or job.
   - **Significance**: Helps identify delays in processing.
   - **Source**: Four Golden Signals.

4. **Traffic**: Tracks the number of requests or jobs processed.
   - **Significance**: Monitors workload and system usage.
   - **Source**: Four Golden Signals.

5. **Errors**: Measures the rate of failed requests or jobs.
   - **Significance**: Identifies system or application issues.
   - **Source**: Four Golden Signals.

6. **Saturation**: Tracks resource utilization (e.g., CPU, memory).
   - **Significance**: Ensures resources are not overloaded.
   - **Source**: Four Golden Signals.

7. **Job Throughput**: Measures the number of jobs processed per unit time.
   - **Significance**: Tracks system efficiency and capacity.
   - **Source**: Batch Job-Specific Metrics.

8. **Job Failure Rate**: Tracks the percentage of failed jobs.
   - **Significance**: Identifies reliability issues in job execution.
   - **Source**: Batch Job-Specific Metrics.

9. **Job Retry Count**: Tracks the number of retries for failed jobs.
   - **Significance**: Helps in diagnosing recurring issues.
   - **Source**: Batch Job-Specific Metrics.

10. **Utilization**: Measures the percentage of resource usage.
    - **Significance**: Ensures optimal resource allocation.
    - **Source**: USE Method.

11. **Job Duration**: Measures the time taken to process individual jobs.
    - **Significance**: Tracks job performance and identifies slow jobs.
    - **Source**: RED Method.

12. **Job Rate**: Tracks the number of jobs processed per second.
    - **Significance**: Monitors system throughput.
    - **Source**: RED Method.

13. **Job Error Count**: Tracks the count of errors during job execution.
    - **Significance**: Identifies recurring issues in job processing.
    - **Source**: RED Method.

14. **Job Resource Saturation**: Tracks the degree to which resources are overloaded during job execution.
    - **Significance**: Ensures system stability and prevents crashes.

## Files Included

1. `performance_metrics.csv`: Contains the list of metrics in keyword form for Prometheus scraping.
2. `Grafana/dashboard.json`: Grafana dashboard configuration file.
3. `README.md`: This file, explaining the metrics and their significance.

## Sources

- Test Code Analysis
- Four Golden Signals
- RED Method
- USE Method
- Batch Job-Specific Metrics