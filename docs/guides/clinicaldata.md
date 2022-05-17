



CLINICALDATA_MEDICATIONTAKING_MEASUREMENTS_V1_VIEW and condition classifiction should link to a parent please create a ticket to resolve.


## CLINICALDATA_ALLERGIES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| ALLERGYID| tbc |  Int 64| |NO|
| ALLERGYNAME| tbc | Character| 200|YES|
| COMMENTS| tbc | Character| 200|YES|
| DATASOURCE| tbc | Character| 500|YES|
| ENDDATE| tbc | Date Time| |YES|
| REACTION1| tbc | Character| 500|YES|
| REACTION2| tbc | Character| 500|YES|
| REACTION3| tbc | Character| 500|YES|
| SEVERITY1| tbc | Character| 500|YES|
| SEVERITY2| tbc | Character| 500|YES|
| SEVERITY3| tbc | Character| 500|YES|
| ALLERGYSOURCE| tbc | Character| 500|YES|
| STARTDATE| tbc | Date Time| |YES|
| STATUS| tbc | Character| 500|YES|
| TYPE| tbc | Character| 500|YES|
| TYPECODES| tbc | Character| 500|YES|
| ALLERGYCODES| tbc | Character| 500|YES|
| CODESYSTEM| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_ALLERGYACTIVES_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| ALLERGYACTIVEID| tbc |  Int 64| |YES|
| CURRENTLYACTIVE| tbc | Character| 20|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_BLOODPRESSURE_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| BLOODPRESSUREMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 1000|YES|
| MEASUREMENT| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| MEASUREMENTSITE| tbc | Character| 500|YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| OBSERVATIONMETHOD| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_BODYMASS_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| BODYMASSMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTASNUMBER| tbc | Decimal fixed-point| 4 decimal places|YES|
| MEASUREMENTASTEXT| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| SOURCESYTEM| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_CONDITION_CLASSIFICATIONS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CONDITIONCLASSIFICATIONID| tbc |  Int 64| |YES|
| CLASSIFICATION| tbc | Character| 20|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
| CREATEDBY | joins to USERS_V1_VIEW. | Cardinality is one-to-many. An alert joins to 1 user. |
| CLOSEDBY | Joins to USERS_V1_VIEW.| Cardinality is zero-to-one. An alert joins to 1 user if closed. |
| ALERTID | Joins to ALERT_NOTIFICATIONS_V1_VIEW.| Cardinality is zero-to-many. |

## CLINICALDATA_CONDITION_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| CONDITIONID| tbc |  Int 64| |NO|
| CODINGSYSTEM| tbc | Character| 500|YES|
| CONDITIONCODES| tbc | Character| 200|YES|
| CONDITIONNAME| tbc | Character| 500|YES|
| DATASOURE| tbc | Character| 500|YES|
| STARTDATE| tbc | Date Time| |YES|
| ENDDATE| tbc | Date Time| |YES|
| STATUS| tbc | Character| 500|YES|
| SOURCE| tbc | Character| 200|YES|
| COMMENTS| tbc | Character| 1000|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_COVERAGE_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| COVERAGEID| tbc |  Int 64| |NO|
| STARTDATE| tbc | Date Time| |YES|
| ENDDATE| tbc | Date Time| |YES|
| GROUPDESCRIPTIONEMR| tbc | Character| 500|YES|
| PLANDESCRIPTIONEMR| tbc | Character| 500|YES|
| SUBGROUPDESCRIPTIONEMR| tbc | Character| 500|YES|
| MEMBERIDEMR| tbc | Character| 200|YES|
| PRECEDENCEEMR| tbc | Character| 500|YES|
| STATUS| tbc | Character| 200|YES|
| SOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_HEART_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| HEARTMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| MEASUREMENTASTEXT| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTMETHOD| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| SOURCESYTEM| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_HEIGHT_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| HEIGHTMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENT| tbc | Character| 500|YES|
| MEASUREMENTUNIT| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_LABS_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| LABMEASUREMENTID| tbc |  Int 64| |NO|
| LABCODE1| tbc | Character| 500|YES|
| LABCODINGSYSTEM1| tbc | Character| 500|YES|
| LABCODE2| tbc | Character| 500|YES|
| LABCODINGSYSTEM2| tbc | Character| 500|YES|
| BODYSITEDISPLAY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 200|YES|
| INTERPRETATION| tbc | Character| 500|YES|
| LABSNAMESTRING| tbc | Character| 500|YES|
| MEASUREMENTMETHODDISPLAY| tbc | Character| 500|YES|
| MEASUREMENTUNITSSTRING| tbc | Character| 500|YES|
| MEASUREMENTDATE| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VALUEASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| VALUE| tbc | Character| 500|YES|
| RESULTDATE| tbc | Date| |YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_MEDICATION_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| MEDICATIONID| tbc |  Int 64| |NO|
| MEDICATIONCODES| tbc | Character| 200|YES|
| MEDICATIONNAME| tbc | Character| 200|YES|
| CODINGSYSTEM| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURE| tbc | Character| 500|YES|
| DURATION| tbc | Character| 50|YES|
| FREQUENCY| tbc | Character| 100|YES|
| INSTRUCTIONS| tbc | Character| 200|YES|
| QUANTITYASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| QUANTITYASTEXT| tbc | Character| 100|YES|
| REASON| tbc | Character| 500|YES|
| ROUTE| tbc | Character| 200|YES|
| SIGCODE| tbc | Character| 200|YES|
| SOURCE| tbc | Character| 200|YES|
| DATE| tbc | Date Time| |YES|
| STARTDATE| tbc | Date Time| |YES|
| ENDDATE| tbc | Date Time| |YES|
| STATUS| tbc | Character| 50|YES|
| STRENGTH| tbc | Character| 100|YES|
| TYPE| tbc | Character| 200|YES|
| ORDEREDBY| tbc | Character| 200|YES|
| ORDEREDDATE| tbc | Date Time| |YES|
| PRESCRIPTIONNUMBER| tbc | Character| 200|YES|
| PRESCRIBEDDATE| tbc | Date Time| |YES|
| PRESCRIBEDBY| tbc | Character| 200|YES|
| FILLDATE| tbc | Date Time| |YES|
| PHARMACY| tbc | Character| 200|YES|
| REVIEWSTATUS| tbc | Character| 200|YES|
| LASTREFILLDATE| tbc | Date Time| |YES|
| REFILLS| tbc | Character| 200|YES|
| REFUSEDREASON| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_MEDICATIONTAKING_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| MEDICATIONTAKINGID| tbc |  Int 64| |YES|
| CURRENTLYTAKING| tbc | Character| 20|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_OXYGEN_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| OXYGENMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTASNUMBER| tbc | Decimal fixed-point| 4 decimal places|YES|
| MEASUREMENTASTEXT| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCESYTEM| tbc | Character| 500|YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_RESPIRATORY_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| RESPIRATORYMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENT| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_RISKS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| RISKID| tbc |  Int 64| |NO|
| CATEGORY| tbc | Character| 200|YES|
| DATASOURCE| tbc | Character| 200|YES|
| DATE| tbc | Date Time| |YES|
| RISKTYPE| tbc | Character| 200|YES|
| NAME| tbc | Character| 200|YES|
| SCOREASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| SCOREASTEXT| tbc | Character| 200|YES|
| SOURCE| tbc | Character| 200|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_TEMPERATURE_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| TEMPERATUREMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTASNUMBER| tbc | Decimal fixed-point| 4 decimal places|YES|
| MEASUREMENTASTEXT| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| MEASUREMENTSITE| tbc | Character| 500|YES|
| MEASUREMENTMETHOD| tbc | Character| 500|YES|
| SOURCE| tbc | Character| 500|YES|
| SOURCESYTEM| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_WAIST_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| WAISTMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| MEASUREMENTASTEXT| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_WAISTTOWEIGHT_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| WAISTTOWEIGHTMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENT| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|

## CLINICALDATA_WEIGHT_MEASUREMENTS_V1_VIEW


| Attribute | Description | Domain definition |Size | Nulls allowed |
| :-------------- | :------ |:------ |:------ |:------ |
| CLIENTREFERENCE| tbc | Character| 200|YES|
| WEIGHTMEASUREMENTID| tbc |  Int 64| |NO|
| CODE1| tbc | Character| 500|YES|
| CODINGSYSTEM1| tbc | Character| 500|YES|
| CODE2| tbc | Character| 500|YES|
| CODINGSYSTEM2| tbc | Character| 500|YES|
| MEASUREMENTASNUMBER| tbc | Decimal fixed-point| 2 decimal places|YES|
| MEASUREMENTASTEXT| tbc | Character| 500|YES|
| MEASUREMENTUNITS| tbc | Character| 500|YES|
| DISPLAYMEASUREMENTUNITS| tbc | Character| 500|YES|
| MEASUREMENTDATETIME| tbc | Date Time| |YES|
| SOURCE| tbc | Character| 500|YES|
| STATUS| tbc | Character| 500|YES|
| VERIFIEDBY| tbc | Character| 500|YES|
| COMMENTS| tbc | Character| 500|YES|
| DATASOURCE| tbc | Character| 500|YES|
| INGESTIONTIME| tbc | Date Time| |YES|

### Links to other data

Please review and amend, just examples below to help your edits.

| Attribute | Description |Cardinality |
| :-------------- | :------ |:------ |
| CLIENTREFERENCE| Joins to CLIENTS_V1_VIEW. | Cardinality is one-to-many.  A client has zero-to-many alerts|
