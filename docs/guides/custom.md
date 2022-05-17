

This section describes data available for custom client data.




## CUSTOM_ENTITIES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| ALERTID|  Identifier for a record.  |  Int 64|--- |NO|
| CLIENTREFERENCE| Unique reference number that identifies the client in the application. | Character| 200|NO|
| UPDATEDBY | The identifier for a user record. The identifier value is an email address.|  NO|
| DATATYPENAME| tbc | Character| 200|YES|
| CATEGORY| Category that the custom client data type is grouped into. For example, Contact, Demographic, Clinical. | Character| 100|NO|
| CLUSTER| Name of a cluster that is configured for a custom client data type that contains attributes. This is populated only when the custom data type contains attributes. | Character| 200|YES|
| POSITION| tbc |  Int 64| |NO|
| ATTRIBUTE| The name of the attribute within the custom entity. | Character| 120|NO|
| VALUE| Value that was entered for the attribute, in string format. | Character| 2000|YES|
| DOUBLEVALUE|  If the base data type of the attribute is a float or decimal, this field displays a numeric double value that you can use for comparisons or arithmetic. Otherwise, this field is blank. | Double floating-point| |YES|
| LONGVALUE|  If the base data type of the attribute is an integer, this field displays a number that you can use for comparisons or arithmetic. Otherwise, this field is blank. |  Int 64| |YES|
| DATEVALUE| Date and time the custom data was created or last updated by a user in the Care Team application. | Date Time| |YES|
| EVIDENCETYPEVERSIONDEFID| tbc |  Int 64| |YES|
| RELATEDPERSON| tbc |  Int 64| |YES|
| EFFECTIVEVERSION| The version number of the custom client data type that applies to a particular effective date. The version number for the very first instance of a custom client data type is 0. Version numbers restart when a version is effective from a new date. |  Int 64| |YES|
| EFFECTIVEFROM| The date from when the custom client data type version became effective. Each version of a client data type is effective from a particular date, and remains effective until the next version is created. | Date| |YES|
| STATUS| Status of the custom client data version, Active or Canceled. | Character| 200|NO|
| INGESTIONTIME| Date and Time the record was ingested, supports change data capture. | Date Time|---  |NO|


### Links to other data

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| UPDATEDBY | Joins to USERS_V1_VIEW.| Cardinality is one-to-one. A custom entity attribute joins to 1 user. |
