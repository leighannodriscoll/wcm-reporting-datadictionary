

This section describes data available for utilizations and actively managed patients.


This section describes data available for patients under active managment.





## PATIENTS_UNDER_MANAGEMENT_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| MONTHYEAR| tbc | Date| |NO|
| PATIENTID| tbc |  Int 64| |NO|
| MONTH| tbc | Character| 40|NO|
| YEAR| tbc |  Int 32| |NO|
| ACTIVELYMANAGEDDAYS| tbc |  Int 32| |NO|
| RECORDSTATUS| tbc | Character| 40|NO|
| UNIQUEREF| tbc | Character| 200|YES|
| FIRSTNAME| tbc | Character| 200|YES|
| LASTNAME| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| -| - | -|



## UTILIZATIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| UTILIZATIONID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| ATTENDEDDATE| tbc | Date| |YES|
| ADMITTEDIND| tbc | Character| 1|YES|
| DISCHARGEDDATE| tbc | Date| |YES|
| OTHERSOURCE| tbc | Character| 500|YES|
| OTHERTYPE| tbc | Character| 200|YES|
| OTHERLOCATION| tbc | Character| 500|YES|
| OTHERDISPOSITION| tbc | Character| 500|YES|
| ADDEDBY| tbc | Character| 256|YES|
| CREATEDON| tbc | Date Time| |YES|
| TYPE| tbc | Character| 200|YES|
| DISPOSITION| tbc | Character| 200|YES|
| SOURCE| tbc | Character| 200|YES|
| LOCATION| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |
