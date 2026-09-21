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

Fixed the error detections using the log_level from "log"

In aiops_pipeline.py :

Fixed by changing the producer_topic to topic

Fixed by changing the consumer_topic to topic to use the same topic as the producer

## Task 6

Executed the pipeline. Screenshot in docs.

# Part 5: Document Your Findings

## Task 7: Update the README

1. 
