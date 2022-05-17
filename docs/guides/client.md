

This section describes data available for clients.

These views groups data items that relate to a client's demographic information, address and contact information. It also contains views that groups data that relates to tags recorded for clients and a view that groups data that shows who has requested emergency access to a client and when.

## CLIENTS_V1_VIEW

This view groups attributes that relate to client's demographics data such as their name, marital status, and gender. In addition, this view groups a client's preferred or most recently updated address, phone number, and email address data.

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|YES|
| PRIORITY| Priority of the item, High, Medium, or Low or Not Set.| Character| 20|YES|
| PRIORITYSORTORDER| Order that the priority values are shown in the report, 1, 2, 3, or 4. |  Int 32|--- |NO|
| CLIENTSTATUS| Client's status in the application, Active or Inactive. | Client's status in the application, Active or Inactive.|20|YES|
| PREFERREDLANGUAGE| Client's preferred language for communications.| Character| 50|YES|
| PREFCOMMMETHOD| Client's preferred method of communication, Hard Copy, Email, Data Transfer, Phone or Fax. | Character| 50|YES|
| DATEOFBIRTH| Client's date of birth. | Date Time|--- |YES|
| DATEOFDEATH| Client's date of death. |--- |YES|
| MOTHERSBIRTHLASTNAME| Mother's birth last name.  | Character| 200|YES|
| BIRTHLASTNAME| Client's birth last name. | Character| 200|YES|
| TYPEOFNAME| Client's type of name, Alias, Preferred, Registered, or Stage Name. | Character| 50|YES|
| FIRSTNAME| Client's first name.  Character| 200|YES|
| LASTNAME| Client's last name.| Character| 200|YES|
| SUFFIX| Client's suffix, for example, Junior, Senior, or Esquire. | Character| 20|YES|
| MIDDLENAME|Client's middle name.  | Character| 200|YES|
| INITIALS|Client's initials. | Character| 50|YES|
| TITLE| Client's title, for example, Mr or Ms. | Character| 20|YES|
| GENDER| Client's gender. | Character| 20|YES|
| MARITALSTATUS| Client's marital status.  | Character| 50|YES|
| PREFERREDID| Client's preferred identification number. | Character| 200|YES|
| PREFERREDIDTYPE| Client's preferred identification type, for example, Reference Number, or Employee ID. | Character| 50|YES|
| PHONETYPE| Type of phone number, Home, Work, Mobile, or Other. By default, the client's preferred phone number is displayed. If no preferred phone number is recorded, the most recently updated phone number is displayed. | Character| 40|YES|
| PHONECOUNTRYCODE| Phone county code.  | Character| 20|YES|
| PHONEAREACODE| Phone area code. | Character| 20|YES|
| PHONENUMBER| Phone number. | Character| 40|YES|
| PHONEEXTENSION| Phone extension number.| Character| 20|YES|
| PHONEPREFERREDIND| Indicates if this is the client's preferred phone number for contact. | Character| 1|YES|
| EMAILADDRESS| Client's email addresss | Character| 500|YES|
| EMAILADDRESSTYPE| Type of email address, Personal, Business, or Other. By default, the client's preferred email address is displayed. If no preferred email address is recorded, the most recently updated email address is displayed. | Character| 40|YES|
| EMAILPREFERREDIND| Indicates if this is the client's preferred email address for contact. | Character| 1|YES|
| CREATIONDATE| Date that the record was created. | Date Time|--- |YES|
| REGISTEREDBYUSER| First name and last name of the user who created the record. | Character| 256|YES|
| ADDRESSTYPE| Type of address, Residential, Work, or Mailing. By default, the client's preferred address is displayed. If no preferred address is recorded, the most recently updated address is displayed.| Character| 40|YES|
| ADDRESSCITY| Address City | Character| 100|YES|
| ADDRESSSTATE| Address State | Character| 100|YES|
| ADDRESSZIP| Address Zip | Character| 30|YES|
| ADDRESS1| Line 1 of the address. | Character| 1024|YES|
| ADDRESS2| Line 2 of the address. | Character| 1024|YES|
| ADDRESS3| Line 3 of the address.| Character| 1024|YES|
| ADDRESSPREFERREDIND| Indicates if this is the client's preferred address for communications. | Character| 1|YES|
| ADDRESSPHYSICALVISIT| Indicates whether the address is the client's physical visit address. The address shown matches the address that is displayed throughout Watson Care Manager for the client, for example, in their Context pane and search result. | Character| 1|YES|

### Links to other data

The attribute CLIENTREFERENCE is the primary key to this table, and can be used to join to any other table if CLIENTREFERENCE is present.

| Attribute | Joins to|Cardinality |
| :-------------- | :------ |:------ |
| REGISTEREDBY | USERS_V1_VIEW | Created-by joins to a user.<br /> A user is assoicated withs to zero-to-many alerts. |

## CLIENT_ADDRESSES_V1_VIEW

This view groups attributes that relate to a client's address such as the address details, address type, and whether the address is the client's preferred address.


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|YES|
| ADDRESSTYPE| Type of address, Residential, Work, Mailing| Character.| 40|YES|
| PREFERREDIND| Indicates if this is the client's preferred address for communication. | Character| 1|NO|
| COMMENTS| Comments entered for the record. | Character| 1024|YES|
| CITY| City | Character| 100|YES|
| STATE| State | Character| 100|YES|
| ZIP| ZIP Code | Character| 30|YES|
| ADD1| Line 1 of the Address | Character| 1024|YES|
| ADD2| Line 2 of the Address | Character| 1024|YES|
| ADD3| Line 3 of the address | Character| 1024|YES|
| PRIORITY| Priority of the item.  |  Int 32|--- |YES|
| PHYSICALVISIT| Indicates whether the address is the client's physical visit address. | Character| 1|YES|
| FROMDATE|Date on which the record type is valid from.| Date|--- |YES|
| ENDDATE|Date on which the record type is valid to.| Date| ---|YES|
| LASTWRITTEN| Date and time the record was changed.| Date Time|--- |YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time|--- |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Joins to |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |




## CLIENT_IDENTIFICATIONS_V1_VIEW
This view groups attributes that relate to client's identification types such as their Employee ID or passport, and the number associated with the identification type.

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|NO|
| ALTERNATEIDTYPE| Client identification type, for example, Reference Number, or Passport Number. The type can be the client's unique system reference number or a configured identification type.  | Character| 50|NO|
| ALTERNATEID| Client's identification number. | Character| 200|NO|
| PREFERREDIND| Indicates if this is the client's preferred identification number for communications. | Character| 1|NO|
| COMMENTS| Comments entered for the record. | Character| 50|YES|
| LASTWRITTEN| Date and time the record was changed. | Date Time|--- |NO|
| FROMDATE| Date on which the record type is valid from. | Date|--- |YES|
| ENDDATE| Date on which the record type is valid to. | Date|--- |YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time|--- |YES|

### Links to other data

| Attribute | Joins to|Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| CLIENTS_V1_VIEW | Client reference joins to a client.<br /> A client is assoicated with zero-to-many alerts.|


## CLIENT_EMAILS_V1_VIEW
This view groups attributes that relate to a client's email address such as the email address details, email address type, and whether the email address is the client's preferred email address.

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|YES|
| EMAILADDRESS| Client's email address. | Character| 500|YES|
| EMAILADDRESSTYPE| Type of email address, Personal, Business, or Other. For each type, only the email address with the most recent start date is displayed. If two email addresses of the same type share the most recent start date, the email address which was modified most recently is displayed. | Character| 40|YES|
| PREFERREDIND| Indicates if this is the client's preferred email address for communications. | Character| 1|NO|
| COMMENTS| Comments entered for the record.| Character| 1024|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time|--- |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Joins to |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE|  CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY |  USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |


## CLIENT_PHONES_V1_VIEW
This view groups attributes that relate to a client's phone number such as the phone number, phone type, and whether the phone number is the client's preferred phone number for calls and texts.

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|YES|
| PHONECOUNTRYCODE| Phone country code. | Character| 20|YES|
| PHONEAREACODE| Phone area code. | Character| 20|YES|
| PHONENUMBER| Phone number. | Character| 40|YES|
| PHONEEXTENSION| Phone extension. | Character| 20|YES|
| PHONETYPE| Type of phone number, Home, Work, Mobile, or Other.| Character| 40|YES|
| PREFERREDIND| Indicates if this is the client's preferred phone number for contact | Character| 1|NO|
| COMMENTS| Comments entered for the record. | Character| 1024|YES|
| PREFERREDFORTEXT| Indicates if this is the client's preferred phone number for texts | Character| 1|YES|
| FROMDATE| Date on which the record type is valid from. | Date| ---|YES|
| ENDDATE| Date on which the record type is valid to.| Date| ---|YES|
| CORRECTIONSETID| Idenfier for the correction set. | Character| 128|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time| ---|YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Joins to |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY |  USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY |USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |

## EMERGENCYACCESS_V1_VIEW
This view groups attributes that relate to emergency access requests. Use this view to identify users who have requested emergency access to a client.

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| EMERGENCYACCESSID| Identifier for a record. |  Int 64|--- |NO|
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|NO|
| REQUESTEDBY| The identity of the user who requested emergency access. The identifier value is an email address. | Character| 256|NO|
| REQUESTEDBYFULLNAME| First name and last name of the user who requested emergency access. | Character| 524|NO|
| REQUESTEDBYROLE| Role of the user who requested emergency access. | Character| 200|NO|
| STATUS| Status of access, active or expired. | Character| 50|NO|
| STARTDATETIME| Date and time when emergency access started. | Date Time| ---|YES|
| LASTACCESSEDDATETIME| Date and time the user last accessed the individual's plan. | Date Time|--- |YES|
| SECURITYROLE| Displays a comma separated list of the user's assigned security roles. | Character | Character| 1024|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time|--- |NO|

### Links to other data



| Attribute | Joins to|Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE|  CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many emergency access request.|
| REQUESTEDBY |  USERS_V1_VIEW | Cardinality is one-to-many. A request is associate with one user |

## TAGS_V1_VIEW

This view groups attributes that relate to a client's tags, such as additional information that describes them like whether they are a member of an organization or group, for example, Student, Football Team.

| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| TAGID| Identifier for a record. |  Int 64|--- |NO|
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|YES|
| TAGNAME| The name of the tag. | Character| 512|YES|
| ADDEDBYUSERNAME| First name and last name of the user who added the record. | Character| 256|YES|
| ADDEDON| Date on which the record was added. | Date Time|--- |YES|
| UPDATEDBYUSERNAME| First name and last name of the user who updated the record. | Character| 256|YES|
| UPDATEDON| Date on which the record was updated. | Date Time| ---|YES|
| STATUS| The tag status, Active or Canceled. | Character| 200|YES|
| INGESTIONTIME| Date and time the record was ingested, supports change data capture. | Date Time|--- |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Joins to |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE|  CLIENTS_V1_VIEW | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY |USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |

## CLIENT_GENDER_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application | Character| 200|YES|
| GENDERID| tbc |  Int 64| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| GENDER| tbc | Character| 20|YES|
| STARTDATE| tbc | Date| |YES|
| ENDDATE| tbc | Date| |YES|
| COMMENTS| tbc | Character| 8000|YES|
| INGESTIONTIME|Date and Time the record was ingested, supports change data capture.| Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## CLIENT_ADDRESS_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| ADDRESSID| tbc |  Int 64| |YES|
| ADDRESSTYPE| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW| Cardinality is zero-to-many. |



## CLIENT_BIRTHDEATH_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| BIRTHDEATHID| tbc |  Int 64| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| DATEOFBIRTH| tbc | Date| |YES|
| DATEOFDEATH| tbc | Date| |YES|
| MOTHERSBIRTHLASTNAME| tbc | Character| 200|YES|
| BIRTHLASTNAME| tbc | Character| 200|YES|
| COMMENTS| tbc | Character| 8000|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## CLIENT_EMAIL_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size| Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application | Character| 200|YES|
| EMAILID| tbc |  Int 64| |YES|
| EMAILTYPE| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| INGESTIONTIME|Date and Time the record was ingested, supports change data capture. | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |






## CLIENT_IDENTIFICATION_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application | Character| 200|YES|
| IDENTIFICATIONID| tbc |  Int 64| |YES|
| IDENTIFICATIONTYPE| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| INGESTIONTIME|Date and Time the record was ingested, supports change data capture. Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## CLIENT_MARITALSTATUS_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application | Character| 200|YES|
| MARITALSTATUSID| tbc |  Int 64| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| MARITALSTATUS| tbc | Character| 50|YES|
| STARTDATE| tbc | Date| |YES|
| ENDDATE| tbc | Date| |YES|
| COMMENTS| tbc | Character| 8000|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## CLIENT_NAME_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application | Character| 200|YES|
| NAMEID| tbc |  Int 64| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| TYPEOFNAME| tbc | Character| 50|YES|
| FIRSTNAME| tbc | Character| 200|YES|
| LASTNAME| tbc | Character| 200|YES|
| SUFFIX| tbc | Character| 20|YES|
| MIDDLENAME| tbc | Character| 200|YES|
| INITIALS| tbc | Character| 50|YES|
| TITLE| tbc | Character| 20|YES|
| COMMENTS| tbc | Character| 8000|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture.| Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## CLIENT_PHONE_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| Unique reference number that identifies the client in the application | Character| 200|YES|
| PHONEID| tbc |  Int 64| |YES|
| PHONETYPE| tbc | Character| 40|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDON| tbc | Date Time| |YES|
| EVIDENCEDESCRIPTORID| tbc |  Int 64| |YES|
| CORRECTIONSETID| tbc | Character| 128|YES|
| ACTION| tbc | Character| 40|YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |


## CLIENT_STATUS_HISTORIES_V1_VIEW


| Attribute | Description | Domain definition |Character size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CONCERNROLESTATUSHISTORYID| tbc |  Int 64| |NO|
| CLIENTREFERENCE| tbc | Character| 200|YES|
| STATUS| tbc | Character| 50|YES|
| STATUSREASON| tbc | Character| 50|YES|
| STATUSOTHERREASON| tbc | Character| 200|YES|
| COMMENTS| tbc | Character| 8000|YES|
| UPDATEDBYFULLNAME| tbc | Character| 524|YES|
| UPDATEDBYROLE| tbc | Character| 200|YES|
| UPDATEDON| tbc | Date Time| |YES|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |
