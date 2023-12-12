
# Create a custom role and add 'Azure role assignments' to have the permission in your subscription to find, start & stop resources


[![Deploy To Azure](https://raw.githubusercontent.com/MCSEdwin/Templates/main/deploytoazure.svg?sanitize=true)] (https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FMCSEdwin%2FTemplates%2Fmain%2FManage_My_Resources_Operator.json)

In order for the application to have the permission in your subscription to find, start & stop resources, the user assigned identity 'ManageMy-Resources' must be assigned a subscription level role. We recommend using a custom role with a minimal set of permissions.

Create custom role
Select the managed resource group (this can be found in the overview section of the managed application).
Select the user assigned identity named 'ManageMy-Resources'
Select 'Azure role assignments'
Add a role assignment at the subscription level granting either the Contributor role or 'Manage My Resources Operator' custom role
Contributor: easy win, suitable for testing the product, but grants the application far more rights than it requires
Manage My Resources Operator: prefered option, assigns the minimum set of rights required to discover, stop and start resources

Documentation for these roles can be found in https://learn.microsoft.com/en-us/azure/role-based-access-control/resource-provider-operations.
