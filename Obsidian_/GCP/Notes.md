## **Question 2 — Database selection**

**Scenario:** A financial application requires a globally distributed relational database with strong consistency, horizontal scalability, high availability and ACID transactions.

**Cloud Spanner**

A globally distributed relational database designed for strong consistency, relational SQL and horizontal scaling.

Why not the others?

|Service|Primary use case|Why not here?|
|---|---|---|
|Cloud SQL|Managed relational database|Scaling and global distribution constraints|
|Firestore|NoSQL document database|Not a relational SQL database|
|Bigtable|Wide-column NoSQL|Not designed for relational ACID transactions|
|Spanner|Globally distributed relational DB|Best fit|


Google Cloud IAM follows this basic model:

**Principal**

Developer / Service Account

**Role**

Specific permissions, e.g. Compute Instance Admin

**Resource**

Project / Folder / Individual resource

For example:

- Team A gets permissions on Project A.
    
- Team B gets permissions on Project B.
    
- Neither team gets unnecessary access to the other's resources.


## **Question 4 — Hybrid networking**

**Scenario:** An enterprise wants high-bandwidth, predictable, private connectivity between its data centre and Google Cloud.

Correct answer: B — Dedicated Interconnect

**Why B is correct**

[Hybrid and multicloud network architectures | Google Cloud Blog](https://images.openai.com/static-rsc-4/kVckkOv3hY010j0zKnQ218MchxGlKHC9TKjDpKCqtvJmceY0RQ-wBeUQo2XhymzmUcPYOebxX6o5_S8RMVw6Zg4J2NNReRd3adBhmuHkrptNpQGXRiHL-9ybAWnWOwAM7Za7Z8xBNBmxtp4OR3Ipqq0GES0xh63NPgC6y6wxmGA?purpose=inline)

**Cloud Interconnect**

Provides dedicated physical connectivity between an on-premises network and Google Cloud.

Compare the options:

|Option|Purpose|
|---|---|
|Cloud VPN|Encrypted connectivity over the internet|
|Dedicated Interconnect|Dedicated private physical connectivity|
|Public IP|Public internet access|
|Cloud NAT|Outbound internet connectivity for private resources|