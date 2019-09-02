This template allows you to deploy a Storage Account with SAS   in azure  subscription.
The storage account provides a unique namespace for your Azure Storage data that is accessible from anywhere in the world over HTTP or HTTPS. An Azure storage account contains all of your Azure Storage data objects: blobs, files, queues, tables, and diskData in your Azure storage account is durable and highly available, secure, and massively scalable.  

Run the below script in Azure cloud shell
------------------------------------------------------------------------------------------------------------------------------ az group deployment create --resource-group GLOBAL-C4E-INT-DEV-EUS-RG --template-uri https://raw.githubusercontent.com/kirantangudu/Master-ARMTemplates/master/StrogewithSas/deploymentTemplate.json
------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------

Below parameters is passed from parameters JSON file to template file.

Parameter Name                            Description
-----------------------------------------------------------------------------------------
storageNamePrefix         The prefix string to add to a generated string that is unique to the resourceGroup
location                  Location where resources will be deployed . List of location -	East US,West US,South Central US,North Europe,East Asia,Japan East,West 			       Europe,Southeast Asia,Japan West,North Central US,Central US,Brazil South,East US 2,Australia Southeast,Australia
                          Location for all resources.
------------------------------------------------------------------------------------------------------------------------------------------------------

