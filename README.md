# event-driven-apps-cosmosdb

# Additional notes:

In order to be able to execute the Github action workflow, you need to:

1 - create a resource group

The resource group will be referred as {resourceGroupName}.

2 - create an app registration with with

clientId
clientSecret
subscriptionId
tenantId

3 - add Github repository secrets for:

- AZURE_RG
- AZURE_SUBSCRIPTION
- AZURE_CREDENTIALS
{
    clientId
    clientSecret
    subscriptionId
    tenantId
}

4 - at a command prompt,

navigate to the app registration -> Managed Application in ...

The {objectID} property will be referred as the servicePrincipalID...

az login

az role assignment create --assignee {servicePrincipalID} --role Owner --scope /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}