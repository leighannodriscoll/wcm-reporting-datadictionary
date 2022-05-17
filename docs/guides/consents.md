

This section describes data available for alerts.


## CONSENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CONSENTID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| CARETEAMMEMBERID| tbc |  Int 64| |YES|
| CONSENTTYPES| tbc | Character| 4000|YES|
| TYPE| tbc | Character| 200|YES|
| RECEIVEDDATE| tbc | Date| |YES|
| RECEIVEDBY| tbc | Character| 256|YES|
| EXPIRYDATE| tbc | Date| |YES|
| STATUS| tbc | Character| 200|YES|
| DESCRIPTION| tbc | Character| 8000|YES|
| WITHDRAWNDATE| tbc | Date| |YES|
| WITHDRAWNBY| tbc | Character| 256|YES|
| ISCOMMUNITYCONSENT| tbc | Date Time| |YES|
| RELATEDTYPE| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many consent records|
| RECEIVEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| WITHDRAWNBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |


## CONSENT_ATTACHMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CONSENTID| tbc |  Int 64| |NO|
| ADDEDBY| tbc | Character| 256|YES|
| ADDEDBYFULLNAME| tbc | Character| 524|YES|
| ADDEDBYROLE| tbc | Character| 200|YES|
| ATTACHMENTNAME| tbc | Character| 1024|YES|
| STATUS| tbc | Character| 200|YES|
| RECEIPTDATE| tbc | Date Time| |YES|
| ISCOMMUNITYCONSENT| tbc | Date Time| |YES|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| ATTACHMENTID| tbc |  Int 64| |NO|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CONSENTID| Joins to CONSENTS_V1_VIEW . | Cardinality is one-to-many.  A client has zero-to-many alerts|
| ADDEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |

## CONSENT_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CONSENTHISTORYID| tbc |  Int 64| |YES|
| UPDATEDBY| tbc | Character| 200|YES|
| UPDATEDDATE| tbc | Date| |YES|
| RELATEDTYPE| tbc | Character| 200|YES|
| STATUS| tbc | Character| 200|YES|
| CONSENTID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CONSENTID| Joins to CONSENTS_V1_VIEW . | Cardinality is one-to-many.  A client has zero-to-many alerts|
| UPDATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
