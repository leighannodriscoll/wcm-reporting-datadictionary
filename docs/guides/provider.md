

This section describes data available for providers.




## PROVIDERS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDERID| tbc |  Int 64| |NO|
| NAME| tbc | Character| 500|YES|
| PHONECOUNTRYCODE| tbc | Character| 20|YES|
| PHONEAREACODE| tbc | Character| 32|YES|
| PHONENUMBER| tbc | Character| 80|YES|
| PHONEEXTENSION| tbc | Character| 60|YES|
| EMAILADDRESS| tbc | Character| 256|YES|
| WEBSITE| tbc | Character| 400|YES|
| STATUS| tbc | Character| 200|YES|
| STARTDATE| tbc | Date| |NO|
| CREATEDBY| tbc | Character| 256|NO|
| CQCPROVIDERID| tbc | Character| 80|YES|
| PAYPALSIGNUP| tbc | Character| 1|NO|
| DESCRIPTION| tbc | Character| 2000|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| -| - | -  |





## PROVIDER_ADDRESSES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDERID| tbc |  Int 64| |NO|
| STATUS| tbc | Character| 200|YES|
| PRIMARYADDRESS| tbc | Character| 1|NO|
| COUNTRY| tbc | Character| 200|YES|
| ADD1| tbc | Character| 1024|YES|
| ADD2| tbc | Character| 1024|YES|
| ADD3| tbc | Character| 1024|YES|
| CITY| tbc | Character| 100|YES|
| STATE| tbc | Character| 100|YES|
| ZIP| tbc | Character| 30|YES|
| PROVIDERADDRESSID| tbc |  Int 64| |YES|
| ADDRESSID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| PROVIDERID| Joins to PROVIDERS_V1_VIEW. | Cardinality is zero-to-many.  A provider has zero-to-many alerts|

## PROVIDER_CONNECT_USERS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDERID| tbc |  Int 64| |NO|
| FIRSTNAME| tbc | Character| 260|YES|
| LASTNAME| tbc | Character| 260|YES|
| PHONECOUNTRYCODE| tbc | Character| 20|YES|
| PHONEAREACODE| tbc | Character| 32|YES|
| PHONENUMBER| tbc | Character| 80|YES|
| PHONEEXTENSION| tbc | Character| 60|YES|
| EMAIL| tbc | Character| 1024|YES|
| STATUS| tbc | Character| 200|YES|
| REQUESTSENT| tbc | Date Time| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| PROVIDERID| Joins to PROVIDERS_V1_VIEW. | Cardinality is zero-to-many.  A provider has zero-to-many alerts|

## PROVIDER_CONTACTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDERID| tbc |  Int 64| |NO|
| FIRSTNAME| tbc | Character| 260|YES|
| LASTNAME| tbc | Character| 260|YES|
| ROLE| tbc | Character| 200|YES|
| PRIMARYCONTACT| tbc | Character| 1|NO|
| PHONECOUNTRYCODE| tbc | Character| 20|YES|
| PHONEAREACODE| tbc | Character| 32|YES|
| PHONENUMBER| tbc | Character| 80|YES|
| PHONEEXTENSION| tbc | Character| 60|YES|
| MOBILEPHONECOUNTRYCODE| tbc | Character| 20|YES|
| MOBILEPHONEAREACODE| tbc | Character| 32|YES|
| MOBILEPHONENUMBER| tbc | Character| 80|YES|
| MOBILEPHONEEXTENSION| tbc | Character| 60|YES|
| EMAILADDRESS| tbc | Character| 256|YES|
| PROVIDERCONTACTLINKID| tbc |  Int 64| |YES|
| PROVIDERCONTACTID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| PROVIDERID| Joins to PROVIDERS_V1_VIEW. | Cardinality is zero-to-many.  A provider has zero-to-many alerts|

## PROVIDER_IDENTIFICATIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDERID| tbc |  Int 64| |NO|
| IDENTIFICATIONNUMBER| tbc | Character| 72|NO|
| IDENTIFICATIONTYPE| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| PROVIDERID| Joins to PROVIDERS_V1_VIEW. | Cardinality is zero-to-many.  A provider has zero-to-many alerts|

## PROVIDER_SERVICE_ADDRESSES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDEROFFERINGID| tbc |  Int 64| |NO|
| STATUS| tbc | Character| 200|YES|
| COUNTRY| tbc | Character| 200|YES|
| ADD1| tbc | Character| 1024|YES|
| ADD2| tbc | Character| 1024|YES|
| ADD3| tbc | Character| 1024|YES|
| CITY| tbc | Character| 100|YES|
| STATE| tbc | Character| 100|YES|
| ZIP| tbc | Character| 30|YES|
| PROVIDERADDRESSID| tbc |  Int 64| |YES|
| ADDRESSID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| PROVIDERID| Joins to PROVIDERS_V1_VIEW. | Cardinality is zero-to-many.  A provider has zero-to-many alerts|

## PROVIDER_SERVICE_CONTACTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDEROFFERINGID| tbc |  Int 64| |NO|
| FIRSTNAME| tbc | Character| 260|YES|
| LASTNAME| tbc | Character| 260|YES|
| ROLE| tbc | Character| 200|YES|
| PRIMARYCONTACT| tbc | Character| 1|NO|
| PHONECOUNTRYCODE| tbc | Character| 20|YES|
| PHONEAREACODE| tbc | Character| 32|YES|
| PHONENUMBER| tbc | Character| 80|YES|
| PHONEEXTENSION| tbc | Character| 60|YES|
| MOBILEPHONECOUNTRYCODE| tbc | Character| 20|YES|
| MOBILEPHONEAREACODE| tbc | Character| 32|YES|
| MOBILEPHONENUMBER| tbc | Character| 80|YES|
| MOBILEPHONEEXTENSION| tbc | Character| 60|YES|
| EMAILADDRESS| tbc | Character| 256|YES|
| PROVIDERCONTACTLINKID| tbc |  Int 64| |YES|
| PROVIDERCONTACTID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| -| - | -|

## PROVIDER_SERVICE_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDEROFFERINGID| tbc |  Int 64| |NO|
| STATUS| tbc | Character| 100|YES|
| STARTDATETIME| tbc | Date Time| |NO|
| CLOSEDDATE| tbc | Date| |YES|
| RECORDEDBY| tbc | Character| 256|NO|
| REASON| tbc | Character| 2000|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## PROVIDER_SERVICE_RATES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDEROFFERINGID| tbc |  Int 64| |NO|
| RATE| tbc | Decimal fixed-point| 2 decimal places|NO|
| STARTDATE| tbc | Date| |NO|
| ENDDATE| tbc | Date| |YES|
| UNITTYPE| tbc | Character| 100|YES|
| PROVIDEROFFERINGRATEID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## PROVIDER_SERVICES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDERID| tbc |  Int 64| |NO|
| PROVIDEROFFERINGID| tbc |  Int 64| |NO|
| SERVICEOFFERINGID| tbc |  Int 64| |NO|
| PROVIDEROFFERINGGROUPID| tbc |  Int 64| |NO|
| NAME| tbc | Character| 200|YES|
| GROUPNAME| tbc | Character| 200|YES|
| LANGUAGES| tbc | Character| 500|YES|
| STATUS| tbc | Character| 200|YES|
| CATEGORIES| tbc | Character| 1000|YES|
| CQCLOCATIONID| tbc | Character| 80|YES|
| ADDEDON| tbc | Date Time| |YES|
| ADDEDBY| tbc | Character| 256|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## PROVIDER_SHORTLISTED_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| PROVIDEROFFERINGID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| SHORTLISTEDBYUSERNAME| tbc | Character| 256|YES|
| SHORTLISTEDBYEXTERNALUSER| tbc | Character| 400|NO|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
