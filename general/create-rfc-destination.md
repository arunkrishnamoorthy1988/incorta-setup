# Create RFC Destination

To configure the callback connector, we need to create an RFC Destination in the SAP system.

To create a new destination, go to transaction code `SM59`.

<img src="general/assets/images/rfc-destintation-create-step1.png" width="700" />

Enter the following details in the create screen.

1. Name of the RFC Destination
2. Description
3. Choose the activation type as "Registerd Server Program"
4. Enter the Program ID for registerd server program.
5. Enter the gateway host and service name.
   Gateway Host - IP address or Host name of the server
   Gateway Service - sapgw<instance_number>.

<img src="general/assets/images/rfc-destintation-create-step2.png" width="700" />

Navigate to the Unicode Tab and select the communication type as Unicode.

<img src="general/assets/images/rfc-destintation-create-step3.png" width="700" />

Click on Save button to save the settings.
