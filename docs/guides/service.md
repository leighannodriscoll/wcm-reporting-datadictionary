

This section describes data available for services.





## SERVICE_BARRIERS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BARRIERID| tbc |  Int 64| |NO|
| SERVICEID| tbc |  Int 64| |NO|
| SERVICENAME| tbc | Character| 200|YES|
| BARRIERNAME| tbc | Character| 1024|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## SERVICE_GOALS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| GOALID| tbc |  Int 64| |NO|
| SERVICEID| tbc |  Int 64| |NO|
| GOALNAME| tbc | Character| 500|YES|
| SERVICENAME| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## SERVICES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| SERVICEDELIVERYID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| PROVIDEROFFERINGID| tbc |  Int 64| |YES|
| SERVICEOFFERINGID| tbc |  Int 64| |NO|
| PROVIDERID| tbc |  Int 64| |YES|
| NAME| tbc | Character| 200|YES|
| DESCRIPTION| tbc | Character| 1000|YES|
| STATUS| tbc | Character| 200|YES|
| CATEGORIES| tbc | Character| 1000|YES|
| UNITVALUE| tbc | Character| 32|YES|
| UNITVALUEASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| UNITTYPE| tbc | Character| 100|YES|
| STARTDATE| tbc | Date| |YES|
| CREATIONDATE| tbc | Date| |NO|
| EXPECTEDENDDATE| tbc | Date| |YES|
| COMPLETIONDATE| tbc | Date| |YES|
| FREQUENCY| tbc | Character| 200|YES|
| UNITCOST| tbc | Decimal fixed-point| 2 decimal places|YES|
| OUTCOME| tbc | Character| 200|YES|
| CREATEDBY| tbc | Character| 256|NO|
| COMPLETEDBY| tbc | Character| 256|YES|
| PAYMENTAUTHSTATUS| tbc | Character| 200|YES|
| AUTHSTATUSUPDATEDON| tbc | Date| |YES|
| AUTHSTATUSUPDATEDBY| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |
