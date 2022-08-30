# Get Data

**RequestType**: `GET_DATA`

To verify the data extraction using synchronous mode of execution,use the request type `GET_DATA`.
The synchronous extractions support output

1. With compression
2. Without Compression

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
| IN_EXTRACTION_METHOD   | SYNCHRONOUS      |
| IN_REQUEST_TYPE        | GET_DATA         |
| IN_SELECTED_TABLE_NAME | ZINC_CONFIG_PROP |
| IN_COMPRESSION_ENABLED | N                |

If you would like to test the data with compression, modify the input parameter `IN_COMPRESSION_ENABLED` to `Y`.

<img src="sap-tables/assets/images/get-data.png" width="700" />

#### Step 3: Execute the function module.

Press the function keyword `F8` or `Execute Button` to execute the function module.

You must be seeing result in one of the Dynamic Tables.

<img src="sap-tables/assets/images/get-data-output.png" width="700" />

Click on the Table displaying output to view the contents.

<img src="sap-tables/assets/images/get-data-output-detail.png" width="700" />
