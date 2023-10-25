# Installing a Package With Package Parameters

## Purpose

This Deployment Plan is an example of deploying a package using an Advanced Deployment Step, in this case to provide a package parameter during deployment.

The example passes the `/InstallDir` parameter to the `python312` package, causing the package to be installed to the location provided.

We use the Advanced Deployment Step to do this because the Basic Deployment Step does not allow package parameters to be used.

## Usage

The Deployment Step installs the `python312` package ([available on the Chocolatey Community Repository](https://community.chocolatey.org/packages/python312)) if it's not already present.

Ensure the package is available on a configured source and set the Target Groups for the Deployment Step.

### Setting the Target Group

You will need to set a Target Group for the Deployment Step:

- Mouse-over the Deployment Step and click the `Edit` button.
    ![Editing a Deployment Step](/images/EditDeploymentStep.jpg)

- Navigate to the `Select Target Groups` panel.

- Highlight your preferred groups and click the `>` button to move them into `Selected Groups`.
    ![Selecting Target Groups](/images/SelectingTargetGroups.jpg)

- Click `Save`.

You are now ready to [move your Deployment Plan to Ready and run it](https://docs.chocolatey.org/en-us/central-management/usage/website/deployments#move-to-ready).