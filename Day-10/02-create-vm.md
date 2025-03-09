# Create VM using Azure CLI

### Start with creating a Resource Group

```
az group create --name learn-azure-cli --location eastus
```

### Set the Resource Group as default (Optional)

```
az config set defaults.group=learn-azure-cli
```

### Create VM with Vnet

```
# Create PowerShell variable
$vmName = "TutorialVM1"

az vm create `
    --resource-group rg-muf-test `
    --name testvm `
    --image Ubuntu2204 `
    --vnet-name testvnet `
    --subnet $subnetName `
    --generate-ssh-keys `
    --output json `
    --verbose
```

### Delete the Resource Group to delete all the resources

```
az group delete --name learn-azure-cli
```

