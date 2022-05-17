

This section describes data available for alerts.





## USERS_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| FIRSTNAME| tbc | Character| 260|YES|
| SURNAME| tbc | Character| 260|YES|
| TITLE| tbc | Character| 40|YES|
| FULLNAME| tbc | Character| 524|YES|
| LOGINID| tbc | Character| 256|YES|
| USERSTATUS| tbc | Character| 100|YES|
| ACCOUNTENABLED| tbc | Character| 1|NO|
| CREATIONDATE| tbc | Date| |YES|
| LASTSUCCESSLOGIN| tbc | Date Time| |YES|
| ROLENAME| tbc | Character| 200|YES|
| CAPACITY| tbc |  Int 32| |YES|
| WORKSPACES| tbc | Character| 1024|YES|
| EXTERNALROLENAME| tbc | Character| 1024|YES|
| SECURITYROLE| tbc | Character| 1024|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Joins to|Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY |USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |




