# Request Status

**RequestType**: `REQUEST_STATUS`

To Check the status of the Submitted Job, request status method is executed.

#### Step 1: Execute Function Module

Go to transaction code `SE37` and enter the name of the function module as `ZINC_SAP_ERP_DATA_EXTRACTOR`.
and click on function key `F8` or press `Execute Button`.

#### Step 2: Enter the test data

Before you enter the input, select the case sensitive checkbox.

<img src="sap-tables/assets/images/case-sensitive-param.png" width="700" />

Enter the request type as `REQUEST_STATUS` and pass the GUID of the request.

You can use the same GUID from the SUBMIT_REQUEST use case.

<img src="sap-tables/assets/images/request-status.png" width="700" />

Following is the output.

<img src="sap-tables/assets/images/request-status-output.png" width="700" />

> This error is fine, we did not pass the File transfer mechanisms input while testing SUBMIT_REQUEST
