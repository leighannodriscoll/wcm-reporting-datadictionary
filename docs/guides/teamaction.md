

This section describes data available for team actions.





## TEAMACTION_BARRIERS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BARRIERID| tbc |  Int 64| |NO|
| ACTIONID| tbc |  Int 64| |NO|
| ACTIONNAME| tbc | Character| 1024|YES|
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

## TEAMACTION_PROGRESSCOMMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROGRESSID| tbc |  Int 64| |NO|
| ACTIONID| tbc |  Int 64| |NO|
| CREATIONDATE| tbc | Date Time| |NO|
| CREATEDBY| tbc | Character| 256|NO|
| COMMENTS| tbc | Character| 8000|YES|
| PROGRESS| tbc | Character| 256|YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## TEAMACTIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| ACTIONID| tbc |  Int 64| |NO|
| ASSIGNEDTO| tbc | Character| 256|YES|
| ASSIGNEDTOFULLNAME| tbc | Character| 524|YES|
| ASSIGNEDTOTEAMROLE| tbc | Character| 200|YES|
| NAME| tbc | Character| 1024|YES|
| CATEGORY| tbc | Character| 100|YES|
| STATUS| tbc | Character| 100|YES|
| ADDEDBY| tbc | Character| 200|NO|
| ADDEDON| tbc | Date| |NO|
| REASON| tbc | Character| 2000|YES|
| STARTDATE| tbc | Date| |NO|
| EXPECTEDENDDATE| tbc | Date| |YES|
| COMPLETEDON| tbc | Date| |YES|
| COMPLETEDBY| tbc | Character| 200|YES|
| OUTCOME| tbc | Character| 100|YES|
| PROGRESS| tbc | Character| 256|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |
