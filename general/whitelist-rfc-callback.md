# Whitelist RFC Callback

For the SAP System to be able to call the incorta server and send the data back, the incorta IP address needs to be whitelist on the SAP System. This information has to be maintained in the Security and Registration info file.

The path to the Security and Registration info files can be found using the following parameters.

1. gw/reg_info
2. gw/sec_info

To view Registration info File path. Go to the transaction code `RZ11`.

Enter the profile name as `gw/reg_info` and click on display.

<img src="general/assets/images/profile-parameter-4.png" />

To View the Security info file path. Go to the transation code `RZ11`.

Enter the profile name as `gw/sec_info` and click on display.

<img src="general/assets/images/profile-parameter-5.png" />

If the SAP Kernel version is 753 or above, these whitelisting of the Host IP address can be done from the SAP Server itself.

### Security Info File

To maintain the whitelist, navigate to the transaction code `SMGW`.

In the top menu bar choose the following.

Go To -> Expert Functions -> External Security -> Maintain ACL Files.

<img src="general/assets/images/smgw-maintain-acl.png" />

> If you do not find this file. Then the kernel version could be lower and you need to modify the files by logging into operating system. The file path can be found in the parameters mentioned above.

<img src="general/assets/images/smgw-maintain-acl-sec-create.png" />

To maintain security file, in the Secinfo file tab, in the toolbar click on the Create button and choose the option standard.

<img src="general/assets/images/smgw-maintain-acl-sec-create-1.png" />

In the pop-up that appears enter the following details.

P/D: Enter the value as P to provide permision.
TP: Name of the JCO Program as mentioned in the RFC destination (INCORTA_JCO_SERVER)
User: Enter the name of the Incorta Data Extraction user. E.g (IDA_EXT_USER)
Host: Hostname or IP address of the Incorta Analytics Server. For the Cloud deployment, we will need a static ip address to be configured.
User-Host: Enter \* to provide full access.

<img src="general/assets/images/smgw-maintain-acl-sec-create-1.png" />

Click on enter or the tick button to add the updated information to the Security Info File.

<img src="general/assets/images/smgw-maintain-acl-sec-create-2.png" />

After enter you can see an entry added to the Security information file.

<img src="general/assets/images/smgw-maintain-acl-sec-create-3.png" />

Click on the save button to save the changes.

### Registration info file.

In the Reginfo tab, click on Create-> Standard in the toolbar to add a new entry.

<img src="general/assets/images/smgw-maintain-acl-reg-create-1.png" /> 

In the popup enter the details and click on Enter or the tick button to add the entry to the file.

P/D: Enter the value as P to provide permision.
TP: Name of the JCO Program as mentioned in the RFC destination (INCORTA_JCO_SERVER)
Host: Hostname or IP address of the Incorta Analytics Server. For the Cloud deployment, we will need a static ip address to be configured.
Access: \*
Cancel: \*

<img src="general/assets/images/smgw-maintain-acl-reg-create-2.png" />

A new entry will be added to reg info file.

<img src="general/assets/images/smgw-maintain-acl-reg-create-3.png" />

Click on the save button to save the changes.

For the SAP Version with kernel less then 753, these options will not be available. Please contact basis support to add this information into the file from operating system.
