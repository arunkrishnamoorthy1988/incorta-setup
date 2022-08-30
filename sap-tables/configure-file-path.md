# Configure File Path

For Asynchronous extraction that does do not use the Common Shared Drive, require the File to be created in the SAP Server first and then transported to the Incorta Server.

If the asynchronous extraction fails, check if the file path is properly configured.

Go to the transaction code `FILE`. Select the `OLD Transaction Code` if the system asks for popup confirmation.

<img src="sap-tables/assets/images/file-path-logical.png" width="700" />

Select `ZINC_INCORTA` and click on assignment of path.

<img src="sap-tables/assets/images/ass-of-path.png" width="700" />

Click on Unix / Windows Operating system as per the system infrastructure where SAP server is hosted.

Check if the physical path directory maintained here is created in the Server.

<img src="sap-tables/assets/images/physical-path.png" width="700" />

To confirm if the path is available.

Go to transaction code `AL11` and check if the directory exists.

<img src="sap-tables/assets/images/incorta-path.png" width="700" />
