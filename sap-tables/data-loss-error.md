# Data Loss Error

If you come across an error where the data count in SAP does not match with the data extracted in the incorta, it is possible it could be one of the following reasons.

1. Check for memory dumps.

In the transaction code `ST22` check if you see any dumps related to Memory allocation associated to the incorta user.
It is possible that you are using chunking and some of the chunk volumes are large and the SAP internal table has no memory to accomadate that.

Resolution: Reduce the chunk size to minimize the error.

2. Multi Node Server

In case if the server has multiple application server node instance it is possible that during parallell processing the data gets written across multiple application server node. To avoid it make sure we have a dedicated parallel server group for the Incorta and the same in configured in `ZINC_CONFIG_PROP` table.

In case of chunking it is possible that jobs are submitted across multiple node, to avoid that make sure we have the Job Server group created and configured in `ZINC_CONFIG_PROP` table.
