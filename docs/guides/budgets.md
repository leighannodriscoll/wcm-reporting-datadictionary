

This section describes data available for budgets.



## BUDGETS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BUDGETID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| ROWNUM| tbc |  Int 64| |YES|
| WEEKLYBUDGETAMOUNT| tbc | Decimal fixed-point| 2 decimal places|YES|
| STARTDATE| tbc | Date| |YES|
| ENDDATE| tbc | Date| |YES|
| REASON| tbc | Character| 200|YES|
| COMMENTS| tbc | Character| 900|YES|
| ADDEDON| tbc | Date Time| |YES|
| ADDEDBY| tbc | Character| 524|YES|
| STATUS| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| ADDEDON | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| ADDEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |



## BUDGET_CONTRIBUTIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BUDGETCONTRIBUTIONID| tbc |  Int 64| |NO|
| BUDGETID| tbc |  Int 64| |NO|
| CONTRIBUTORNAME| tbc | Character| 200|YES|
| APPROVALTYPE| tbc | Character| 200|YES|
| CONTRIBUTIONAMOUNT| tbc | Decimal fixed-point| 2 decimal places|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| BUDGETID| Joins to BUDGETS_V1_VIEW. | Cardinality is zero-to-many.  A budget has zero-to-many contributions|


## BUDGET_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| BUDGETID| tbc |  Int 64| |NO|
| STATUS| tbc | Character| 200|YES|
| UPDATEDON| tbc | Date Time| |YES|
| UPDATEDBY| tbc | Character| 256|YES|
| DRAFTAMOUNT| tbc | Decimal fixed-point| 2 decimal places|YES|
| STATUSCOMMENT| tbc | Character| 900|YES|
| UPDATEDAMOUNT| tbc | Decimal fixed-point| 2 decimal places|YES|
| BUDGETHISTORYID| tbc |  Int 64| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| BUDGETID| Joins to BUDGETS_V1_VIEW. | Cardinality is zero-to-many.  A budget has zero-to-many contributions|
| UPDATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |

## BUDGET_SERVICES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| SERVICEDELIVERYID| tbc |  Int 64| |NO|
| BUDGETID| tbc |  Int 64| |NO|
| INGESTIONTIME| tbc | Date Time| |YES|
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

### Links to other data



| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| BUDGETID| Joins to BUDGETS_V1_VIEW. | Cardinality is zero-to-many.  A budget has zero-to-many contributions|
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CREATEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| COMPLETEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
