
This section describes data available for barriers.





## BARRIERS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BARRIERID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| NOTEID| tbc |  Int 64| |YES|
| NAME| tbc | Character| 1024|YES|
| CATEGORY| tbc | Character| 100|YES|
| STATUS| tbc | Character| 100|YES|
| ADDEDBY| tbc | Character| 200|NO|
| ADDEDON| tbc | Date Time| |NO|
| RESOLVEDBY| tbc | Character| 200|YES|
| RESOLVEDON| tbc | Date| |YES|
| NOTETEXT| tbc | Character| 1024|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| RESOLVEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |



PLEASE ADD IN BARRIER_NOTES_V1_VIEW.....
