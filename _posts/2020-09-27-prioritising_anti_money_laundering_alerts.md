---
layout: "post"
title:  "Prioritsing anti-money laundering alerts"
date:   2020-08-30 12:14:00 +1300
---

We estimated that by using our machine learning model: 
- 90% of the more serious alerts could be identified before lunch time 
- 50% of the more serious alerts could be identified within the first hour of the day  
![alert_prioritisation](/assets/alert_prioritisation.png){: width="560"}

And we have achieved the following milestones to be able to come up with the estimated benefits. 

1. We prepared to start. We have 
- gone through, together, which data fields to extract  
- decided and implemented a way to pseudonymised the account number  
- set up secured storage both on our on-premise server and on the cloud  
- shown examples of how the output could look like in the frontend and backend 


1. We went through a few trials and extracted 2 iterations of data  
- We have had help from our platform developers and our customer, which is much appreciated.  


1. We validated the accuracy of the extracted data. We have: 
- estimated the data to be 90% accurate - good for proof-for-concept  
- verified our understanding of the business process / how team works   
- made sure our assumptions of the data are correct so that we handled the data according to the business process  
- cut some corners because it is a proof-for-concept 


1. We made sure to communicate these and that they are acceptable 

1. We prepared to run machine learning algorithms. We have:
- aggregated and transformed the data into something we can feed into ML algorithms  
- generated 500 fields per alert that the feature selection step can choose from  

1. We iterated through the data transformation and the modelling steps. We have:
- applied the state-of-the-art python machine learning packages (sklearn and pyOD)   
- implemented 14 types of algorithms on the prepared and filtered data  
- ach of the 14 algorithms was fine-tuned to identify a champion model  
- rainstormed and implemented some extra steps to further improve model performance 

1. We quantified the benefits that the model can bring. We have:
- ran a scenario in which the analysts would be getting a list of alerts ranked by the machine learning model every day, for half a year
- estimated based on the ranked list that:
		- 50% of the more serious alerts could be identified within the first hour of the day
		- 90% of the more serious alerts could be identified within the first four hours

1. And finally, we wrote this list of milestones 

