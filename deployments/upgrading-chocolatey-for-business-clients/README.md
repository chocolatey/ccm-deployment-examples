# Upgrading Chocolatey for Business Client Components

## Purpose

These Deployment Plans are examples of upgrading the Chocolatey for Business client components.

There are two example Deployment Plans here. They follow the instructions laid out on the [upgrading to Chocolatey v2](https://docs.chocolatey.org/en-us/guides/upgrading-to-chocolatey-v2-v6#upgrade-using-chocolatey-central-management-deployments) page.

The first upgrades the Chocolatey for Business client components to the latest 1.x version.

The second upgrades Chocolatey CLI to the latest version.

## Usage

You should import both the `Latest1x` and `Latest2x` Deployment Plans if you are on a version of Chocolatey CLI older than 1.4.0, and deploy `Upgrade Chocolatey for Business Client to Latest 1.x` first, before deploying `Upgrade Chocolatey for Business Client` to upgrade to the latest version.

If you are upgraded to Chocolatey CLI version 2.0 or above, you can just import and run `Latest2x`.

> Although the ScheduledTasks module is available on Windows Server 2012 R2, the `chocolatey-agent` service encounters an error when trying to import it. It is recommended to explore other options for the scheduled task if you're using Windows Server 2012 R2.

After importing the Deployment Plans, you will need to set the Target Groups for each. We strongly recommend testing this on a smaller group to ensure it works as expected in your environment.

### Importing the Deployment Plans

- Download the `DeploymentPlan-Latest1x.json` and `DeploymentPlan-Latest2x.json` from this directory.

- Login to your Chocolatey Central Management instance.

- Navigate to the `Deployments` tab (on the left navigation bar) and click `Import Deployment`.  
    ![The Deployments selection on the left nav bar, and the Import Deployment button](/images/DeploymentTab.jpg)

- Click `Browse` and select the downloaded `.json` files.  
    ![The Import Deployment Modal](/images/DeploymentImportModal.jpg)

- Click `Import`.

For further details, please see the [documentation](https://docs.chocolatey.org/en-us/central-management/usage/examples/deployments).

### Setting the Target Group

You will need to set a Target Group for the Deployment Steps:

- Mouse-over the Deployment Step and click the `Edit` button.
    ![Editing a Deployment Step](/images/EditDeploymentStep.jpg)

- Navigate to the `Select Target Groups` panel.

- Highlight your preferred groups and click the `>` button to move them into `Selected Groups`.
    ![Selecting Target Groups](/images/SelectingTargetGroups.jpg)

- Click `Save`.

You are now ready to [move your deployment to Ready and run it](https://docs.chocolatey.org/en-us/central-management/usage/website/deployments#move-to-ready).