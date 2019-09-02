This template allows you to deploy a Integration Service Environment  in azure subscription.
The Integration Service Environment (ISE) provides a dedicated Logic Apps runtime that can directly integrate with systems in a virtual network. While creating, it is injected into your Azure virtual network, which allows you to deploy Logic Apps as a service on your VNET.
Below ARM template will be used which creates a virtual network and subnets then deploys an Integration Service Environment (ISE) including non-native connectors.


Run the below script in Azure cloud shell
---------------------------------------------------------------------------------------------------------------------------------------------------
New-AzResourceGroupDeployment -ResourceGroupName sbddevtest1 -TemplateUri https://raw.githubusercontent.com/dhanainfy/DhanaInfy/master/ARMTemplates/integration-service-environment/azuredeploy.json -TemplateParameterUri https://raw.githubusercontent.com/dhanainfy/DhanaInfy/master/ARMTemplates/integration-service-environment/azuredeploy.parameters.json
-------------------------------------------------------------------------------------------------------------------------------------------------------

Run the below script in  windows poweshell
----------------------------------------------------------------------------------------------------------------------------------------------------------
D:\> New-AzResourceGroupDeployment -Name Sbdrgdeployment -ResourceGroupName GLOBAL-C4E-INT-DEV-EUS-RG  -TemplateFile "D:\Dhana\projects\SBD\ARMTemplates\ISE\azuredeploy.json" -TemplateParameterfile "D:\Dhana\projects\SBD\ARMTemplates\ISE\azuredeploy.parameters.json"
-------------------------------------------------------------------------------------------------------------------------------------------------

Below parameters is passed from parameters JSON file to template file.

Parameter Name                            Description
-----------------------------------------------------------------------------------------
integrationServiceEnvironmentName         The name of the Integration Service Environment.
location                                  Location for all resources.
integrationServiceEnvironmentSku          The SKU for the Integration Service Environment, either Developer or Premium.
skuCapacity                               The number of scale units for the Integration Service Environment. 0 is the base unit.
managedConnectors                         The list of managed connectors to deploy into the ISE. The values must be from this list: 						 				  sql;ftp;azureblob;azurefile;azurequeues;azuretables;sftpwithssh;edifact;x12;servicebus;documentdb;eventhubs;
                                          mq;sqldw;db2;smtp;si3270
vnetName                                  The name of the VNET for ISE to be deployed into.
vnetAddressPrefix                         The VNET address prefix. For example, 10.0.0.0/22.
subnet1Prefix				  The prefix for the first ISE subnet. For example, 10.0.1.0/26.
subnet1Name                               The name of the first ISE subnet.
subnet2Prefix				  The prefix for the second ISE subnet. For example, 10.0.1.64/26.
subnet2Name                               The name of the second ISE subnet.
subnet3Prefix                             The prefix for the third ISE subnet. For example, 10.0.1.128/26.
subnet3Name                               The name of the third ISE subnet.
subnet4Prefix                             The prefix for the fourth ISE subnet. For example, 10.0.1.192/26.
subnet4Name                               The name of the fourth ISE subnet.
rebuildVNET                               After the first deployment, you don't need to recreate the VNET. When set to false this will skip the VNET and subnet deployment.
