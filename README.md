## How to create service principle in Azure

1. Install the latest version of [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest) on your machine

1. Run ```az login``` in your command line

   <img src="Images\AzLogin.png" alt="iisconfigure"></img>

1. Browse the URL provided in the command line and copy the code and paset it in the textbox provided. Click on Continue button.

1. Once you logged in successfully, console will display you information related to your subscription.
    ```
    {
        "cloudName": "AzureCloud",
        "id": "****-****-****-****",
        "isDefault": true,
        "name": "YOUR SUBSCRIPTION NAME",
        "state": "Enabled",
        "tenantId": "***-****-****-****",
        "user": {
        "name": "****-****-****-****",
        "type": "user"
        }
    }
    ```

1. Now use the [rbac](https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-cli) command to create service principal 
```az ad sp create-for-rbac --name ServicePrincipalName --password PASSWORD```

    >Replace **ServicePrincipalName** name and **Password**

1. Now you will be returned with the details of your Service Principal created 
    <img src="Images\tenant.png">

    ``` 
    Here the AppID is your Client ID
    Password is your Client Secret
    Tenant is your Tenant ID
    ```
  