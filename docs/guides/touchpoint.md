

This section describes data available for touchpoints.



## TOUCHPOINTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| TOUCHPOINTID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| NOTEID| tbc |  Int 64| |NO|
| ADDEDBY| tbc | Character| 256|YES|
| ADDEDBYFULLNAME| tbc | Character| 524|YES|
| ADDEDBYROLE| tbc | Character| 200|YES|
| ADDEDDATE| tbc | Date Time| |YES|
| CONTACTWITH| tbc | Character| 50|YES|
| CONTACTMETHOD| tbc | Character| 50|YES|
| CONTACTDIRECTION| tbc | Character| 50|YES|
| CONTACTOUTCOME| tbc | Character| 50|YES|
| CONTACTDATETIME| tbc | Date Time| |NO|
| CONTACTDURATION| tbc | Decimal fixed-point| 2 decimal places|YES|
| VALIDATEDIDENTITYIND| tbc | Character| 1|NO|
| SUBJECTTEXT| tbc | Character| 480|YES|
| NOTETEXT| tbc | Character| 32592|YES|
| SENSITIVE| tbc | Character| 1|YES|
| STATUS| tbc | Character| 50|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| ADDEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |



## TOUCHPOINT_COMMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| NOTEID| tbc |  Int 64| |NO|
| AUTHOR| tbc | Character| 100|YES|
| CONTENT| tbc | Character| 32592|YES|
| CREATIONDATE| tbc | Date Time| |YES|
| POSITION| tbc |  Int 32| |NO|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| TOUCHPOINTID| Joins to TOUCHPOINTS_V1_VIEW. | Cardinality is zero-to-many.  A client has zero-to-many alerts|
