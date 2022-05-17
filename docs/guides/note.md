

This section describes data available for notes.




## NOTES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| NOTEID| tbc |  Int 64| |NO|
| ADDEDBY| tbc | Character| 256|YES|
| ADDEDBYFULLNAME| tbc | Character| 524|YES|
| ADDEDBYROLE| tbc | Character| 200|YES|
| PRIORITY| tbc | Character| 20|YES|
| SUBJECT| tbc | Character| 480|YES|
| NOTECONTEXT| tbc | Character| 20|YES|
| STATUS| tbc | Character| 20|YES|
| NOTETYPE| tbc | Character| 50|YES|
| DURATION| tbc |  Int 32| |YES|
| MODIFIEDDATETIME| tbc | Date Time| |YES|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| NOTE| tbc | Character| 32592|YES|
| DISCARDREASON| tbc | Character| 512|YES|
| MODIFIEDBY| tbc | Character| 524|YES|
| SENSITIVE| tbc | Character| 1|YES|
| CREATEDDATETIME| tbc | Date Time| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| ADDEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| MODIFIEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |






## NOTE_COMMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| NOTEID| tbc |  Int 64| |NO|
| NOTETYPE| tbc | Character| 40|NO|
| MODIFIEDDATETIME| tbc | Date Time| |YES|
| POSITION| tbc |  Int 32| |NO|
| AUTHOR| tbc | Character| 100|YES|
| CONTENT| tbc | Character| 32592|YES|
| CREATIONDATE| tbc | Date Time| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| NOTEID| Joins to NOTES_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
