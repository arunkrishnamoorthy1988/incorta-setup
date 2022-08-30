# Get Column List

**RequestType**: `GET_COLUMN_LIST`

This request retuns the metadata of the Tables to be used by Incorta Tables. To get the Metadata the required input is to pass the Schema name and Table name.

#### Step 1: Execute Function Module

Go to transaction code `SE37` and enter the name of the function module as `ZINC_SAP_ERP_DATA_EXTRACTOR`.
and click on function key `F8` or press `Execute Button`.

#### Step 2: Enter the test data

Before you enter the input, select the case sensitive checkbox.

<img src="sap-tables/assets/images/case-sensitive-param.png" width="700" />

Enter the data for the following paramters. For this use case, i have taken the schema name as `Accounting` and the table name as `TPIR2`.

> If you do not know the schema name, enter the schema name as ALL

| Parameter Name          | Parameter Value |
| :---------------------- | :-------------- |
| IN_EXTRACTION_METHOD    | SYNCHRONOUS     |
| IN_REQUEST_TYPE         | GET_COLUMN_LIST |
| IN_SELECTED_SCHEMA_NAME | Accounting      |
| IN_SELECTED_SCHEMA_NAME | Accounting      |
| IN_SELECTED_TABLE_NAME  | TPIR2           |

<img src="sap-tables/assets/images/get-column-list-input.png" width="700" />

#### Step 3: Execute the function module.

Press the function keyword `F8` or `Execute Button` to execute the function module.

You must be seeing result in the output table parameter `OUT_SCHEMA_DEFINITION`

This table returns the list of all application components(Schemas) as well as the tables with their column informations.

<img src="sap-tables/assets/images/get-column-list.png" width="700" />

Click on the Table Entries to view the content of the table.

<img src="sap-tables/assets/images/get-column-list-output.png" width="700" />

> Should these three request types (GET_SCHEMA_LIST, GET_TABLE_LIST and GET_COLUMN_LIST) works fine, you will be able to configure the Tables in the Incorta UI.
