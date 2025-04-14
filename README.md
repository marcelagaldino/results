# Dataset


This repository contains the experimental data and statistical analysis related to the article: *Strengthening Trust in vTPMs: Integrity-Based Anchoring Mechanism for Hyperconverged Environments.*

# Directory Overview

- **memory_utilization**: Include memory usage dataset with statistical analysis
  - *memory_utilization_data.csv*: contains the raw memory usage data collected during the experimental runs.
  - *memory_utilization_summary.csv*: provides summary statistics of memory usage for each experimental scenario and run. 
  - *memory_confidence_intervals.csv*: contains the 95% confidence intervals for memory usage, estimated using a bootstrap resampling approach with 5,000 replicates (n = 5000).
- **cpu_utilization**: Include memory usage dataset with statistical analysis
  - *cpu_utilization_data.csv*: contains the raw cpu usage data collected during the experimental runs.
  - *cpu_utilization_summary.csv*: provides summary statistics of cpu usage for each experimental scenario and run. 
  - *cpu_confidence_intervals.csv*: contains the 95% confidence intervals for cpu usage, estimated using a bootstrap resampling approach with 5,000 replicates (n = 5000).
- **anchoring_time**: Include anchoring time dataset with statistical analysis
  - *anchoring_time_data.csv*: contains the raw anchoring time data collected during the experimental runs.
  - *anchoring_time_summary.csv*: provides summary statistics of anchoring time for each experimental scenario and run.
  - *diff_anchoring_time_remote.csv*: contains the mean differences between local and remote anchoring times
  - *diff_anchoring_time_remote_mtls.csv*: contains the mean differences between local and remote anchoring times with mTLS
  - *anchoring_time_confidence_intervals.csv*: contains the 95% confidence intervals for anchoring time, estimated using a bootstrap resampling approach with 5,000 replicates (n = 5000).
  - *diff_anchoring_time_confidence_intervals_remote.csv*: contains the 95% confidence intervals for mean differences between local and remote anchoring times, estimated using a bootstrap resampling approach with 5,000 replicates (n = 5000).
  - *diff_anchoring_time_confidence_intervals_remote_mtls.csv*: contains the 95% confidence intervals for mean differences between local and remote anchoring times with mTLS, estimated using a bootstrap resampling approach with 5,000 replicates (n = 5000).

 
    
# Data Description

---

| Field                    | Description                                                                 | Type            |
|--------------------------|-----------------------------------------------------------------------------|-----------------|
| `timestamp`              | Time at which the measurement was collected (format: HH:MM:SS)              | `string`        |
| `memory_utilization`     | Instantaneous memory usage in percentage                                    | `float`         |
| `cpu_utilization`        | Instantaneous CPU usage in percentage                                       | `float`         |
| `number_extend`          | Number of extend operations performed during the measurement period         | `integer`       |
| `host_id`                | Identifier of the host machine where the measurement was collected          | `string`        |
| `scenario`               | Label indicating the experimental scenario or configuration                 | `string`        |
| `execution_id`           | Identifier for the specific execution or repetition of the experiment       | `integer`       |
| `mean_memory_utilization`| Average memory usage over a set of measurements                             | `float`         |
| `mean_cpu_utilization`   | Average CPU usage over a set of measurements                                | `float`         |
| `ci_lower`               | Lower bound of the 95% confidence interval for the target metric            | `float`         |
| `ci_upper`               | Upper bound of the 95% confidence interval for the target metric            | `float`         |
| `std`                    | Standard deviation of the measurements                                      | `float`         |
| `min`                    | Minimum observed value                                                      | `float`         |
| `percentile25`           | 25th percentile of the observed values                                      | `float`         |
| `percentile50`           | 50th percentile (median) of the observed values                             | `float`         |
| `percentile75`           | 75th percentile of the observed values                                      | `float`         |
| `max`                    | Maximum observed value                                                      | `float`         |

---

