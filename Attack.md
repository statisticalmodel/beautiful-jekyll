---
layout: page
title: Attack Secutity Analysis
subtitle:  Analysis of Attack data in Networks
---
### Background
Internet and its number of users is growing each year, with it also the number
attacks and security exploits grows. Networks are prone to network attracts and
since the growing number of users and increasing availability of tools for
intruding and hacking, the number of attacks is also growing.
Australian Cyber Security Centre reviewed the levels of sophistication attackers
used in order to compromise networks (ACSC, 2019) and concluded that there
is a need to develop better intrusion detection models.
According to IBM the average cost of a data breach is USD 3.92 million in the year of 2019 (IBM, 2019).


### Data
+ Botnet traffic dataset from IoT networks
+ The dataset suffers from imbalance. _A dataset is considered to be imbalanced when 
the distribution of the classes differs substantially and where the classes of 
interest are rare. This can have the consequence of generating biased results (Fathi Ganji, 2010)._
+ The dataset consist of 1 million observations on 35 attributes from
network traffic. 
+ The data has seven pattern classes, one Normal and six attack classes. 

### Attack classes include
Data Exfiltration, HTTP, Keylogging, OS Fingerprint, Service Scan and TCP attacks.

### Model Used: Random Forest together with Feature Engineered variables
Random Forest has managed to predict network attacks well, Rama et al. used Random
Forest was to predict attacks in the open sorce NSL-KDD dataset (Rama R, 2017)

The model was built on 500 trees with four variables tried in each
split. The model has a _training_ accuracy of 100% and an OOB estimate error of
0.01%.

### Confusion Matrix
<img width="801" alt="Confusion Matrix" src="https://user-images.githubusercontent.com/15735938/109419740-42276000-79cf-11eb-9d4c-4b56ad2b4400.png">

The accuracy of the model is 99.98% and the kappa accuracy is 99.96%. The model achieves a sensitivity score of
over 99% for all the classes except for Data Exfiltration and Keylogging. These
two classes are the smallest within the data, and even though this is a very good
model, it would benefit from having more observations especially for the Data
Exfiltration class. The model achieves a high specificity score for all classes. The
lowest F1 score is found for the Data Exfiltration class and all the other classes
have a very high F1 score. 

#### Other
Mean Decrease Accuracy plot was used to understand which variables that influenced the models most. 

### Construction of Feature engineered variable
<img width="615" alt="feature_engineere" src="https://user-images.githubusercontent.com/15735938/109419413-a0534380-79cd-11eb-9fa9-dbcb80bd9e6c.png">


## Findings 
A set of important variables to identify the network attacks was found. Feature engineered variables properly summarize the behaviours of the
network from the raw network data with good result.
The model managed to classigy all TCP attacks correctly.
There where not enough observations to correctly learn the behaviour for Data Exfiltration.
The model can be used to detect HTTP, Keylogging, OS Fingerprint, Service Scan and TCP attacks.
