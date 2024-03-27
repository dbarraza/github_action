# Pasos para conectar Github con Azure 

### 1. Crear un service principal con rol de contributor sobre toda la suscripción

az ad sp create-for-rbac --name "GitHubDbarrazaMg" --role contributor --scopes /subscriptions/4cc9961d-df65-423e-b1ab-f37088abfcd5/resourceGroups/RgGitHubAction --json-auth

Display name: GitHubDbarrazaMg
SubscriptionId: 4cc9961d-df65-423e-b1ab-f37088abfcd5
Application (client) ID: f030366b-8159-4af8-a634-dda6e9373ec1
SecredId: 61462d4c-0d58-4043-99b6-b6bf43d240a5
SecretValue: qo-8Q~FHzBIRz_Ue-6TztyejwQ8Hg.YLX3wVnbdS
TenantId: 76c87c9d-bdc2-4f37-af73-579aa99fc5f6
````
{
  "clientId": "f030366b-8159-4af8-a634-dda6e9373ec1",
  "clientSecret": "euM8Q~Q-EJieaelwO2O727k1ciL1Y4JBptADkbCb",
  "subscriptionId": "4cc9961d-df65-423e-b1ab-f37088abfcd5",
  "tenantId": "76c87c9d-bdc2-4f37-af73-579aa99fc5f6",
  "activeDirectoryEndpointUrl": "https://login.microsoftonline.com",
  "resourceManagerEndpointUrl": "https://management.azure.com/",
  "activeDirectoryGraphResourceId": "https://graph.windows.net/",
  "sqlManagementEndpointUrl": "https://management.core.windows.net:8443/",
  "galleryEndpointUrl": "https://gallery.azure.com/",
  "managementEndpointUrl": "https://management.core.windows.net/"
}
````

### 2. Agregar el secreto en Github secret con el valor AZURE_CREDENTIALS
