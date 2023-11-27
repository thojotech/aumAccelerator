# Azure Update Manager Accelerator (aumAccelerator)
The Azure Update Manager Accelerator (aumAccelerator) is a set of Azure Bicep templates for implementing all the Azure policies, maintenance configurations, alert rules, action groups, and alert processing rules required to manage software updates of Windows virtual machines in Azure, or Azure Arc-enabled virtual machines on-premise at scale. [Azure Update Manager](https://learn.microsoft.com/en-us/azure/update-manager/overview?tabs=azure-vms) is replacing Azure Update Management with Azure Automation, which is [retiring August 2024](https://azure.microsoft.com/en-us/updates/were-retiring-the-log-analytics-agent-in-azure-monitor-on-31-august-2024/).

## Prerequisites
The aumAccelerator uses a number of Bicep modules from the [ALZ-Bicep](https://github.com/Azure/ALZ-Bicep/) Github repository, and from the [Common Azure Resource Modules Library (CARML)](https://github.com/Azure/ResourceModules) Github repository.

### ALZ-Bicep
I recommend you start with the [ALZ-Bicep accelerator](https://github.com/Azure/ALZ-Bicep/wiki/Accelerator), which will give you the basic framework for successfully implementing the aumAccelerator. After you complete the steps to implement the ALL-Bicep accelerator, copy the aumAccelerator files to ALZ-Bicep\config\custom-modules.

The aumAccelerator uses the policyAssignmentManagementGroup.bicep module to assign the "Configure periodic checking for missing system updates on azure virtual machines" policy definition to the Intermediate root management group. If you are not familar with policy assignment in Azure Landing zones, I recommend you visit the [Azure Enterprise Scale Landing Zone (ESLZ)](https://github.com/Azure/Enterprise-Scale/wiki/ALZ-Policies) architecture documentatione before continuing.

### Common Azure Resource Modules Library (CARML)
