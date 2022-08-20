# Azure Pipelines

This template enables the [flowchart](https://github.com/ProjetaAi/projetaai-starters/blob/main/for_plugins/ci/README.md) designed by projetaai team to work with Azure Pipelines

## How to use it

### Production pipeline (prod.yml)

1. Go to your DevOps repo page
2. Create a new pipeline by going to the `pipelines` page, then hit the `new pipeline` button
3. Select the service you are using to maintain the repo, then choose the desired repo
4. Select `Existing Azure Pipelines YAML`, then type `azure-pipelines/prod.yml` as the path
5. Hit the variables button and add the variables following the table below:

| Variable | Value | Is Secret |
|----------|-------------|--------|
| PRODUCTION_CLIENT_ID | ID of the service principal with access to the production AzureML service | true |
| PRODUCTION_CLIENT_ID | Secret of the service principal with access to the production AzureML service | true |
| PRODUCTION_TENANT_ID | Tenant ID of the service principal with access to the production AzureML service | true |
| PRODUCTION_COMPUTE | Name of the compute instance that is going to run the project | false |
| PRODUCTION_RESOURCE_GROUP | Resource group that holds the production workspace | true |
| PRODUCTION_WORKSPACE | Workspace that holds the production AzureML service | true |

6. Save (and run)

### Development pipeline (dev.yml)

1. Go to your DevOps page
2. Create a new pipeline by selecting `pipelines`, then hit the `new pipeline` button
3. Select the service you are using to maintain the repo, then choose the desired repo
4. Select `Existing Azure Pipelines YAML`, then type `azure-pipelines/dev.yml` as the path
5. Hit the variables button and add the variables following the table below:

| Variable | Value | Is Secret |
|----------|-------------|--------|
| DEVELOPMENT_CLIENT_ID | ID of the service principal with access to the production AzureML service | true |
| DEVELOPMENT_CLIENT_ID | Secret of the service principal with access to the production AzureML service | true |
| DEVELOPMENT_TENANT_ID | Tenant ID of the service principal with access to the production AzureML service | true |
| DEVELOPMENT_COMPUTE | Name of the compute instance that is going to run the project | false |
| DEVELOPMENT_RESOURCE_GROUP | Resource group that holds the production workspace | true |
| DEVELOPMENT_WORKSPACE | Workspace that holds the production AzureML service | true |

6. Save (and run)
