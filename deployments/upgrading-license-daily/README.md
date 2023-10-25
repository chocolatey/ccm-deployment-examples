# Upgrading Chocolatey License Regularly

## Purpose

These Deployment Plans are basic examples of deploying a package on a schedule. In this case `chocolatey.license`.

## Usage

We recommend creating a `chocolatey.license` package when using Chocolatey for Business environments. This ensures you can push out license changes to your client computers.

The Deployment Step upgrades, or installs if not present, the `chocolatey.license` package. If you don't currently have a license package, you can create one by following [the instructions](https://docs.chocolatey.org/en-us/c4b-environments/azure/license-update#creating-a-new-license-package).

There is a second example Deployment Plan that would run weekly.

There are [more options available](https://docs.chocolatey.org/en-us/central-management/usage/website/deployments#recurring-deployments) for scheduling. You can see the required values for your current version of Chocolatey Central Management in the provided swagger document.

After importing the Deployment Plans, you will need to set the Target Groups and `Start Date Time` for each. We recommend using the `All Computers` Target Group. You may also want to change the Deployment Plan name to something more meaningful.

### Importing the Deployment Plans

- Download the `DeploymentPlan.json` from this directory (or the `DeploymentPlan-Weekly.json` example).

- Login to your Chocolatey Central Management instance.

- Navigate to the `Deployments` tab (on the left navigation bar) and click `Import Deployment`.
    ![The Deployments selection on the left nav bar, and the Import Deployment button](/images/DeploymentTab.jpg)

- Click `Browse` and select the downloaded `.json` file.
    ![The Import Deployment Modal](/images/DeploymentImportModal.jpg)

- Click `Import`.

For further details, please see the [documentation](https://docs.chocolatey.org/en-us/central-management/usage/examples/deployments).

### Setting the Start Date Time

Before you can run the Deployment Plan, you must set the `Start Date Time` to a time at least 30 minutes in the future.

To do so, click on the clock icon next to the `Start Date Time` field. When you have selected an appropriate time, click `Save`.

![Updating an invalid Start Date Time](/images/ScheduleStartDateTimeUpdate.jpg)

### Setting the Target Group

You will also need to set a Target Group for the Deployment Step:

- Mouse-over the Deployment Step and click the `Edit` button.
    ![Editing a Deployment Step](/images/EditDeploymentStep.jpg)

- Navigate to the `Select Target Groups` panel.

- Highlight your preferred groups and click the `>` button to move them into `Selected Groups`.
    ![Selecting Target Groups](/images/SelectingTargetGroups.jpg)

- Click `Save`.

You are now ready to [move your deployment to Ready and run it](https://docs.chocolatey.org/en-us/central-management/usage/website/deployments#move-to-ready).