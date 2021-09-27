---
layout: "post"
title:  "What happened within an anomaly detection POC"
date:   2021-08-30 12:14:00 +1300
---

Most if not all rules are one-dimensional. For example, the distribution of transaction amount looks like this for Fexco.  

Rules are designed to cut off at a certain threshold. Every transaction above the threshold raises, which will be reviewed by a compliance officer. This way of raising alerts produces many false alarms or false positives. And it is the primary concern for the financial institutions, as raised in the survey on page 36. 

Anomaly detection takes a multi-dimensional view. It uses a more sophisticated method to combine multiple factors and only raise a flag when all the conditions are met. Anomaly detection is also dynamic. This means that the conditions are customised for each account. 

A modern way to raise alerts would be to:  
- use sensible factors as identified by the compliance officers in creating the rules 
- feed them into a dynamic, rather than a fixated one-dimensional, process 

This is not allowed by the current regulations. The purpose of this anomaly detection POC is to supplement and not to replace alerts raised by current rules. 

What happened within an anomaly detection POC 

1. We extracted non-sensitive data and anonymised the sensitive fields. 
	- The details are listed in page 7 

2. We transform data so that it can be fed into anomaly detection algorithms 
	- we counted the average, smallest, and largest transactions for the past 10 transactions  
	- we identified the most frequent modes, channels, from fund type, to fund type, location for the past 10 transactions  

3. We run a series of open-source state-of-the-art anomaly detection algorithms.

4. We compared which transactions were identified by different types of algorithms as top 100 anomalies
	- for each algorithm, we counted how many identical transactions were also identified by other algorithms 
	- e selected the top algorithm which has the highest number of anomalies that overlapped with other algorithms 

5. We present the top 100 anomalies from the chosen algorithm.
	- we identified the factors behind the each of the 100 anomalies
	- for each of the top 4 factors, we present the context that explains why it contributed to the anomalies
![anomaly_example](/assets/unusual_transaction_example.png){: width="250"}