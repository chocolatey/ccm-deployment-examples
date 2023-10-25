# Installing Multiple Packages

## Purpose

This Deployment Plan is a basic example of deploying multiple packages.

We recommend that you use a separate Deployment Step for each package to deploy to allow per-computer reporting.

You can use this to generate larger Deployment Plans with more comprehensive suites of packages, even mixing Basic and Advanced Deployment Steps in order to provide additional configuration.

## Usage

This Deployment Plan is an example of deploying a selection of software such as a baseline for a company computer or to meet a department's requirements. The Deployment Plan could be scheduled to re-run against a specific group to ensure that the software is always present and up to date.

After importing the Deployment Plan, you will need to set the Target Groups.

### Importing the Deployment

- Download the `DeploymentPlan.json` from this directory (or the `DeploymentPlan-Weekly.json` example).

- Login to your Chocolatey Central Management instance.

- Navigate to the `Deployments` tab (on the left navigation bar) and click `Import Deployment`.  
    ![The Deployments selection on the left nav bar, and the Import Deployment button](/images/DeploymentTab.jpg)

- Click `Browse` and select the downloaded `.json` file.
    ![The Import Deployment Modal](/images/DeploymentImportModal.jpg)

- Click `Import`.

See the [documentation](https://docs.chocolatey.org/en-us/central-management/usage/examples/deployments) for more information.

### Setting the Target Group

You will need to set a Target Group for the Deployment Step:

- Mouse-over the deployment step and click the `Edit` button.
    ![Editing a Deployment Step](/images/EditDeploymentStep.jpg)

- Navigate to the `Select Target Groups` panel.

- Highlight your preferred groups and click the `>` button to move them into `Selected Groups`.
    ![Selecting Target Groups](/images/SelectingTargetGroups.jpg)

- Click `Save`.

You are now ready to [move your deployment to Ready and run it](https://docs.chocolatey.org/en-us/central-management/usage/website/deployments#move-to-ready).