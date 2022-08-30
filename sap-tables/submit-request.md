# SUBMIT Request

**RequestType**: `SUBMIT_REQUEST`

To verify the data extraction using Asynchronous mode of execution,use the request type `SUBMIT_REQUEST`.

#### Step 1: Execute Function Module

Go to transaction code `SE37` and enter the name of the function module as `ZINC_SAP_ERP_DATA_EXTRACTOR`.
and click on function key `F8` or press `Execute Button`.

#### Step 2: Enter the test data

Before you enter the input, select the case sensitive checkbox.

<img src="sap-tables/assets/images/case-sensitive-param.png" width="700" />

For this use case, i have taken the Incorta Global Configuration table which has lesser entry.

Enter the following parameter.

| Parameter Name         | Parameter Value  |
| :--------------------- | :--------------- |
| IN_EXTRACTION_METHOD   | ASYNCHRONOUS     |
| IN_REQUEST_TYPE        | SUBMIT_REQUEST   |
| IN_SELECTED_TABLE_NAME | ZINC_CONFIG_PROP |

<img src="sap-tables/assets/images/submit-request-input.png" width="700" />

#### Step 3: Execute the function module.

Press the function keyword `F8` or `Execute Button` to execute the function module.

In this scenario you will not see the output as Asyncrhronous mode of execution, submits the background program to extract the data.

To view the background program, get the GUID of the extraction.

<img src="sap-tables/assets/images/submit-request-guid.png" width="700" />

#### Step 4: Verify the Job

Go to transaction code `SM37`.

The Job can be formed by concatenating `ZINC_` with the `GUID`.

Example:
GUID: `2022083012182562572107245`

Then Jobname would be: `ZINC_2022083012182562572107245`

Enter the Job name, change username to '\*' and set the appropriate date of Job submitted.

<img src="sap-tables/assets/images/submit-request-job.png" width="600" />

Click on execute.

<img src="sap-tables/assets/images/job-output.png"  />

To view the job log, place the cursor on the Job name and click on Job Log.

<img src="sap-tables/assets/images/job-log.png"  />

<img src="sap-tables/assets/images/job-log-output.png" />
