This template allows you to deploy a Storage in azure subscription.
The storage account provides a unique namespace for your Azure Storage data that is accessible from anywhere in the world over HTTP or HTTPS. An Azure storage account contains all of your Azure Storage data objects: blobs, files, queues, tables, and diskData in your Azure storage account is durable and highly available, secure, and massively scalable.  

Run the below script in Azure cloud shell
---------------------------------------------------------------------------------------------------------------------------------------------------
New-AzureRmDeployment -Name ExampleDevDeploymentsbd -TemplateUri https://csg694c4e354b63x4070xa5b.blob.core.windows.net/templatesdevrg/template.json -TemplateParameterUri https://csg694c4e354b63x4070xa5b.blob.core.windows.net/templatesdevrg/template.parameters.json
-------------------------------------------------------------------------------------------------------------------------------------------------------

Run the below script in  windows poweshell
----------------------------------------------------------------------------------------------------------------------------------------------------------
D:\> New-AzResourceGroupDeployment -Name Sbdrgdeployment -ResourceGroupName GLOBAL-C4E-INT-DEV-EUS-RG  -TemplateFile "D:\Dhana\projects\SBD\ARMTemplates\StorageAccount\azuredeploy.json" -TemplateParameterfile "D:\Dhana\projects\SBD\ARMTemplates\StorageAccount\azuredeploy.parameters.json"
-------------------------------------------------------------------------------------------------------------------------------------------------

Below parameters is passed from parameters JSON file to template file.

Parameter Name                            Description
-----------------------------------------------------------------------------------------
storageNamePrefix         The prefix string to add to a generated string that is unique to the resourceGroup
location                  Location where resources will be deployed . List of location -	East US,West US,South Central US,North Europe,East Asia,Japan East,West 			       Europe,Southeast Asia,Japan West,North Central US,Central US,Brazil South,East US 2,Australia Southeast,Australia
                          Location for all resources.
------------------------------------------------------------------------------------------------------------------------------------------------------

