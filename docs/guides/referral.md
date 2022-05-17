

This section describes data available for referrals.


Referrals are used to direct a client to the correct organization unit that will meet their care management needs.  


## REFERRALS_V1_VIEW

This view groups data items that relate to a client's referrals such as cohort name, referral date, referral reason and stats of the referral. 

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| REFERRALID| tbc |  Int 64|--- |NO|
| COHORTNAME| tbc | Character| 500|YES|
| COHORTSOURCE| tbc | Character| 100|YES|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| REFERRALREASON| tbc | Character| 2000|NO|
| REFERREDDATE| tbc | Date|--- |NO|
| CREATEDBY| tbc | Character| 200|YES|
| STATUS| tbc | Character| 200|YES|
| PRIORITY| tbc | Character| 200|YES|
| FROMORGNAME| tbc | Character| 500|YES|
| FROMORGEXTERNALREF| tbc | Character| 400|YES|
| TOORGNAME| tbc | Character| 500|YES|
| TOORGEXTERNALREF| tbc | Character| 400|YES|
| COMMENTS| tbc | Character| 2000|YES|
| ASSIGNEDTO| tbc | Character| 200|YES|
| ASSIGNEDDATE| tbc | Date Time| ---|YES|
| REJECTREASON| tbc | Character| 200|YES|
| REJECTCOMMENTS| tbc | Character| 2000|YES|
| REJECTOTHERREASON| tbc | Character| 500|YES|
| REJECTEDATE| tbc | Date Time| ---|YES|
| REJECTEDY| tbc | Character| 200|YES|
| OTHERREFERRALREASON| tbc | Character| 2000|YES|
| SOURCE| tbc | Character| 400|YES|
| ORIGINALSOURCE| tbc | Character| 400|YES|
| INGESTIONTIME| tbc | Date Time| ---|YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Joins to |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE|CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| ASSIGNEDTO |  USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| REJECTEDY | USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
