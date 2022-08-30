# Get Tables List

**RequestType**: `GET_TABLE_LIST`

List the tables available for the users, based on the schema provided as input. The user should have access to the table
in order to be listed in the output.

#### Step 1: Execute Function Module

Go to transaction code `SE37` and enter the name of the function module as `ZINC_SAP_ERP_DATA_EXTRACTOR`.
and click on function key `F8` or press `Execute Button`.

#### Step 2: Enter the test data

Before you enter the input, select the case sensitive checkbox.

<img src="sap-tables/assets/images/case-sensitive-param.png" width="700" />

Enter the data for the following paramters. For this use case, i have taken the schema name as `Accounting`.
Alternatively if you dont have the Schema name with you, use the Schema Name as `ALL`.

> ALL Schema returns all the tables available to the user.

| Parameter Name          | Parameter Value |
| :---------------------- | :-------------- |
| IN_EXTRACTION_METHOD    | SYNCHRONOUS     |
| IN_REQUEST_TYPE         | GET_TABLE_LIST  |
| IN_SELECTED_SCHEMA_NAME | Accounting      |

<img src="sap-tables/assets/images/get-table-list-input.png" width="700" />

#### Step 3: Execute the function module.

Press the function keyword `F8` or `Execute Button` to execute the function module.

You must be seeing result in the output table parameter `OUT_SCHEMA_DEFINITION`

This table returns the list of all application components(Schemas) as well as the tables that is available for the schema.

<img src="sap-tables/assets/images/get-table-list.png" width="700" />

Click on the Table Entries to view the content of the table.

<img src="sap-tables/assets/images/get-table-list-output.png" width="700" />

> Copy a schema name and table name to execute the next request type `GET_COLUMN_LIST`.
