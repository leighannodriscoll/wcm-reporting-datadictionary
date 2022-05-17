

This section describes data available for inquiries.





## INQUIRIES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| INQUIRYID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| SERVICEOFFERINGID| tbc |  Int 64| |NO|
| SERVICENAME| tbc | Character| 500|YES|
| REFERENCENUMBER| tbc |  Int 64| |NO|
| RECORDEDON| tbc | Date Time| |YES|
| RECORDEDBY| tbc | Character| 256|YES|
| RESPONSEREQUIREDBY| tbc | Date| |YES|
| UNITTYPE| tbc | Character| 200|YES|
| UNITVALUE| tbc | Character| 50|YES|
| EXPECTEDSTARTDATE| tbc | Date| |YES|
| EXPECTEDENDDATE| tbc | Date| |YES|
| FREQUENCY| tbc | Character| 200|YES|
| STATUS| tbc | Character| 200|YES|
| DAYS| tbc | Character| 500|YES|
| REASON| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data


| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many inquiry|
| RECORDEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |


## INQUIRY_COMMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| INQUIRYID| tbc |  Int 64| |NO|
| RECORDEDON| tbc | Date Time| |NO|
| RECORDEDBY| tbc | Character| 256|NO|
| COMMENT| tbc | Character| 8000|YES|
| INQUIRYEVENTID| tbc |  Int 64| |NO|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| INQUIRYID| Joins to INQUIRIES_V1_VIEW. | Cardinality is one-to-many.  A inquiry has zero-to-many comments|
| RECORDEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |


## INQUIRY_RESPONSES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| INQUIRYLINEITEMID| tbc |  Int 64| |NO|
| INQUIRYID| tbc |  Int 64| |NO|
| PROVIDERID| tbc |  Int 64| |NO|
| SERVICEOFFERINGID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| RESPONDER| tbc | Character| 400|NO|
| STATUS| tbc | Character| 200|YES|
| OFFEREXPIRYDATE| tbc | Date| |YES|
| OFFEREDUNITS| tbc | Character| 32|YES|
| OFFEREDRATE| tbc | Decimal fixed-point| 2 decimal places|YES|
| RECORDEDON| tbc | Date Time| |YES|
| RECORDEDBY| tbc | Character| 256|YES|
| COMMENTS| tbc | Character| 8000|YES|
| ISRESPONSECOMMENT| tbc |  Int 32| |NO|
| TYPE| tbc | Character| 200|NO|
| INQUIRYLINEITEMEVENTID| tbc |  Int 64| |NO|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data


| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| INQUIRYID| Joins to INQUIRIES_V1_VIEW. | Cardinality is one-to-many.  A inquire has zero-to-many responses|
| PROVIDERID| Joins to PROVIDERS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
