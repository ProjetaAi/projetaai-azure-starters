# Azure Pipelines

This template enables the [flowchart](https://github.com/ProjetaAi/projetaai-starters/blob/main/for_plugins/ci/README.md) designed by ProjetaAi team to work with Azure Pipelines

## How to use it

### Production pipeline (prod.yml)

Performs the same procedures as the (dev.yml) pipeline, but also creates the draft pipelines and publishes them on the AzureML workspace.

1. Go to your DevOps repo page
2. Create a service connection with the workspace that contains the AzureML service.
3. Create a new pipeline by going to the `pipelines` page, then hit the `new pipeline` button
4. Select the service you are using to maintain the repo, then choose the desired repo
5. Select `Existing Azure Pipelines YAML`, then type `azure-pipelines/prod.yml` as the path
6. Hit the variables button and add the variables following the table below:

| Variable | Value | Is Secret |
|----------|-------------|--------|
| PRODUCTION_COMPUTE | Name of the compute instance that is going to run the project | false |
| PRODUCTION_RESOURCE_GROUP | Resource group that holds the production workspace | true |
| PRODUCTION_WORKSPACE | Workspace that holds the production AzureML service | true |

6. Save (and run)

> Note: This pipeline implements the full flowchart.

### Development pipeline (dev.yml)

Performs linting and testing on the project.

1. Go to your DevOps page
2. Create a new pipeline by selecting `pipelines`, then hit the `new pipeline` button
3. Select the service you are using to maintain the repo, then choose the desired repo
4. Select `Existing Azure Pipelines YAML`, then type `azure-pipelines/dev.yml` as the path
5. Hit the variables button and add the variables following the table below:
6. Save (and run)
