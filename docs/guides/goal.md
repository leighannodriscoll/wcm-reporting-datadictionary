

This section describes data available for goals.




## GOALS_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| GOALID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| NAME| tbc | Character| 1024|YES|
| FOCUSAREA| tbc | Character| 200|YES|
| TYPE| tbc | Character| 100|YES|
| STAGEOFCHANGE| tbc | Character| 100|YES|
| IMPORTANCE| tbc | Character| 100|YES|
| CONFIDENCE| tbc | Character| 100|YES|
| ADDEDBY| tbc | Character| 200|NO|
| ADDEDON| tbc | Date| |NO|
| COMPLETEDBY| tbc | Character| 200|YES|
| COMPLETEDON| tbc | Date| |YES|
| SOURCE| tbc | Character| 100|YES|
| STARTDATE| tbc | Date| |YES|
| TARGETDATE| tbc | Date| |YES|
| REASON| tbc | Character| 2000|YES|
| OUTCOME| tbc | Character| 100|YES|
| PROGRESS| tbc | Character| 256|YES|
| TARGETVALUE| tbc | Character| 100|YES|
| COMPLETIONCOMMENTS| tbc | Character| 8000|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Joins to |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many alerts|
| COMPLETEDBY | USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID |  ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |

## GOAL_BARRIERS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BARRIERID| tbc |  Int 64| |NO|
| GOALID| tbc |  Int 64| |NO|
| GOALNAME| tbc | Character| 1024|YES|
| BARRIERNAME| tbc | Character| 1024|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| GOALID| Joins to GOALS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many goals|
| BARRIERID | joins to BARRIERS_V1_VIEW. | Cardinality is one-to-many. An goal joins to 1 barrier. |

## GOAL_CLIENTACTIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| GOALID| tbc |  Int 64| |NO|
| ACTIONID| tbc |  Int 64| |NO|
| GOALNAME| tbc | Character| 1024|YES|
| ACTION| tbc | Character| 1024|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| GOALID| Joins to GOALS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many goals|

## GOAL_PROGRESSCOMMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROGRESSID| tbc |  Int 64| |NO|
| GOALID| tbc |  Int 64| |NO|
| CREATIONDATE| tbc | Date Time| |NO|
| CREATEDBY| tbc | Character| 256|NO|
| COMMENTS| tbc | Character| 8000|YES|
| PROGRESS| tbc | Character| 256|YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| GOALID| Joins to GOALS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many goals|

## GOAL_TEAMACTIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| GOALID| tbc |  Int 64| |NO|
| ACTIONID| tbc |  Int 64| |NO|
| GOALNAME| tbc | Character| 1024|YES|
| ACTION| tbc | Character| 1024|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| GOALID| Joins to GOALS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many goals|
