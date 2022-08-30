# Create Role and Assign User to the Role.

To provide necessary permissions required for the Extraction user, we require the extraction user to have access to the following authorization objects
listed in [Extract user profile](https://docs.incorta.com/cloud/references-connectors-sap-erp/#extract-user-profile)

To organize things, we will create two different roles.

1. Base roles ( User permission )
2. Table Role ( Role to provide access to Tables )

### Base Role

#### Step 1: Create the role

Go to transaction `PFCG` and create a new Role.

Enter the name `ZIDA_BASE_ROLE` for the role and click on create.

<img src="general/assets/images/base-role-create.png" width="700" />

Enter the description for the role and click on Save before we assign authorization objects.

<img src="general/assets/images/save-role.png" width="700" />

#### Step 2: Assign the authorizations

Navigate to the authorization tab, and click on the Change Authorization Data.

<img src="general/assets/images/change-auth-data.png" width="700" />

In the pop-up that appears click on `Do not select Templates`.

<img src="general/assets/images/no-def-template.png" width="700" />

Follow the steps to add authorization for all these Authorization objects.

1. [S_RFC](general/auth-srfc.md)
2. [S_TCODE](general/auth-stcode.md)
3. [S_BTCH_ADM](general/auth-btchadm.md)
4. [S_BTCH_JOB](general/auth-btchjob.md)
5. [S_DATASET](general/auth-dataset.md)

The authorization mentioned above are required for communicating to SAP Sever and executing the program.

### Table Role

In order to provide Access tables to be extracted, create a new role following the steps above.

Go to transaction code `PFCG`, enter the name of the role as `ZIDA_TAB_ROLE` and click on create.
Skip the template and create the role.

<img src="general/assets/images/tab-role.png" width="700" />

Enter the description and save the role.

Navigate to the Authorization sections and assign the authorization object. To provide access to the tables names you can use one of the method below.

In the SAP ECC 700 , we do not have the authorization role `S_TABU_NAM`, hence we use the `S_TABU_DIS` to provide access to tables.
In the higher versions than 702 we use the `S_TABU_NAM` to provide access to tables.

1. [S_TABU_DIS](general/auth-tab-dis.md)
2. [S_TABU_NAM](general/auth-tab-name.md)
