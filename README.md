# GitHub Challenge

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hey there!

Your challenge is ready.
Follow the instructions provided for this challenge and complete the required tasks in this repository.

Make sure your work is committed and pushed to your repository before submission.

Good luck!


---

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

---

# Part 1: Set Up and Understand the Environment

## Task 1:

A payment service is being monitored through this data.

It is being monitored that whether a payment is succesfully completed or not.

Through AIops we are monitoring the whole payment system and looking for any system failure in case of a payment being failed


# Part 2: Prepare and Inspect Operational Data

## Task 2:

The fields "response_time_ms", "cpu_percent", "memory_percent" represent the metrics.

The fields "log_level" and "message" are the log type and the log message which represents log informations.

Timestamps are used to get the information about when the error or the fault happened in our service.

The observations with "log_level"= "INFO" appear to represent normal behaviour. 

The observations with "log_level"= "ERROR" appear to represent unusual behaviour. 


# Part 3: Validate Anomaly Detection & Event Streaming Workflow

## Task 3

Fixed the error where the log level checked "WARNING" instead of "ERROR"

One improvement can be using models like Isolation forest to detect anamoly instead of simple rule based fixed metrics check.

## Task 4

Ran and screenshot attached in the docs.


# Part 4: Troubleshoot & Demonstrate the AIOps Workflow

## Task 5

In anomaly_detector.py:

Fixed the error detections using the log_level, changing it from "WARNING" to "ERROR"

In aiops_pipeline.py :

Fixed by changing the producer_topic to topic

Fixed by changing the consumer_topic to topic to use the same topic as the producer

## Task 6

Executed the pipeline. Screenshot in docs.

# Part 5: Document Your Findings

## Task 7: Update the README

1. This is a scenario of AIOps in which we are monitoring a payment service and looking for any failed payments to take action and fix them.

2. The operation data contains 7 fields - 
    1. "timestamp" - The date and time of the log.
    2. "service" - The type of service we are observing, in our case "payment-service"
    3. "response_time_ms" - The response time in ms.
    4. "cpu_percent" - The percentage of CPU used.
    5. "memory_percent" - The percentage of memory used.
    6. "log_level" - The type of log, as per our data "INFO" or "ERROR"
    7. "message" - The message related to the event

3. The data contains 2 error logs

4. The anomaly_detector checks for following thresholds and log_level = "ERROR"
    response_time_threshold=500, cpu_threshold=80, memory_threshold=80

    2 anomalies were found using these

5. The workflow is like this - 
       load_data >> create_topic >> creat_produce >> create_consumer >> detecta anomalies in data >> consume_events >> return anamoly record

6. The following output was found -

    ```
    ==================================================
    AIOps Pipeline Result
    ==================================================
    Records processed: 10
    Anomalies detected: 2
    Events consumed: 2

    Detected Events:

    Service: payment-service
    Timestamp: 2026-09-20T10:05:00
    Type: ANOMALY
    Reasons: High response time, Error log detected

    Service: payment-service
    Timestamp: 2026-09-20T10:06:00
    Type: ANOMALY
    Reasons: High response time, High CPU utilization, High memory utilization, Error log detected
    ```

7. 
    1. In anomaly_detector.py:

        Fixed the error detections using the log_level, changing it from "WARNING" to "ERROR"

    2. In aiops_pipeline.py :

        Fixed by changing the producer_topic to topic

        Fixed by changing the consumer_topic to topic to use the same topic as the producer

8. The current anamoly detction uses a simple threshold to detect the anamolies, We can use other ML models like Isolation Forest to detect these anamolies instead.

9. First clone this repo and then install the requirements.txt in your environment. Edit your anamoly_detection.py and aiops_pipeline.py and fix the errors mentioned. Then Run the aiops_pipeline.py

