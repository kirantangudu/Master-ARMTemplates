This template allows you to deploy a Resource group in azure subscription.
Resource Group is the container that holds related resources for an Azure solution. It will be created by providing name and location. 

Run the below script in Azure cloud shell
---------------------------------------------------------------------------------------------------------------------------------------------------
New-AzDeployment -Name SBDDevDeployment  -TemplateUri https://raw.githubusercontent.com/dhanainfy/DhanaInfy/master/ARMTemplates/ResourceGroup/azuredeploy.json -TemplateParameterUri https://raw.githubusercontent.com/dhanainfy/DhanaInfy/master/ARMTemplates/ResourceGroup/azuredeploy.parameters.json
-------------------------------------------------------------------------------------------------------------------------------------------------------

Run the below script in  windows poweshell
----------------------------------------------------------------------------------------------------------------------------------------------------------
New-AzDeployment -Name SBDDevDeployment  -TemplateUri https://raw.githubusercontent.com/dhanainfy/DhanaInfy/master/ARMTemplates/ResourceGroup/azuredeploy.json -TemplateParameterUri https://raw.githubusercontent.com/dhanainfy/DhanaInfy/master/ARMTemplates/ResourceGroup/azuredeploy.parameters.json
-------------------------------------------------------------------------------------------------------------------------------------------------

Below parameters is passed from parameters JSON file to template file.

Parameter Name                            Description
-----------------------------------------------------------------------------------------
rgName         The name of the Integration Service Environment.
location       Location where resources will be deployed . List of location -	East US,West US,South Central US,North Europe,East Asia,Japan East,West 			       Europe,Southeast Asia,Japan West,North Central US,Central US,Brazil South,East US 2,Australia Southeast,Australia
               Location for all resources.
------------------------------------------------------------------------------------------------------------------------------------------------------

