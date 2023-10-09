# Chocolatey Central Management Deployment Examples

This repository contains a selection of example Deployment Plans that can be imported directly to [Chocolatey Central Management](https://chocolatey.org/solutions/central-management-deployments).

## Importing Deployments

To import one of the example deployments, follow these steps:

- Download the deployment from the repository
- Login to your Chocolatey Central Management instance
- Navigate to the `Deployments` tab (on the left navigation bar) and click `Import Deployment`  
    ![The Deployments selection on the left nav bar, and the Import Deployment button](/images/DeploymentTab.jpg)
- Click `Browse` and select the downloaded json file  
    ![The Import Deployment Modal](/images/DeploymentImportModal.jpg)
- Click `Import`

You should then be able to edit the deployment, select target groups for each step, and kick it off.

For further details, please see the [documentation at docs.chocolatey.org](https://docs.chocolatey.org/en-us/central-management/usage/examples/deployments).

## Contributing

We welcome contributions! Please follow these guidelines when submitting examples to this repository:

- Export your deployment without target groups, even if they target `All Computers`
- Create a readme for the deployment explaining it's purpose, usage, and steps required to import it successfully