# Get Schema List

**RequestType**: `GET_SCHEMA_LIST`

List the schemas available for the users, based on the roles assigned to the user.

To test if the schemas are returning data based on user roles, execute the following.

#### Step 1: Execute Function Module

Go to transaction code `SE37` and enter the name of the function module as `ZINC_SAP_ERP_DATA_EXTRACTOR`.
and click on function key `F8` or press `Execute Button`.

#### Step 2: Enter the test data

Enter the data for the following paramters.

| Parameter Name       | Parameter Value |
| :------------------- | :-------------- |
| IN_EXTRACTION_METHOD | SYNCHRONOUS     |
| IN_REQUEST_TYPE      | GET_SCHEMA_LIST |

#### Step 3: Execute the function module.

Press the function keyword `F8` or `Execute Button` to execute the function module.

You must be seeing result in the output table parameter `OUT_SCHEMA_DEFINITION`

This table returns the list of all application components(Schemas) that is available for the user to extract.

<img src="sap-tables/assets/images/get-schema-list.png" width="700" />

You can see the schema list by clicking on the table.

<img src="sap-tables/assets/images/get-schema-list-output.png" width="700" />

> Copy a schema name to use it in the next test case.
