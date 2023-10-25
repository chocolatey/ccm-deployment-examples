# Installing a Package (Simple)

## Purpose

This Deployment Plan is a basic example of deploying a package using a simple Deployment Step.

## Usage

The only Deployment Step in this Deployment Plan upgrades, or installs if not present, the `Firefox` package ([available on the Chocolatey Community Repository](https://community.chocolatey.org/packages/firefox)).

Assuming this package was available on your sources, you will only need to set the Target Groups for the Deployment Step. If you don't have it available, you can download it using `choco download firefox --source="'https://community.chocolatey.org/api/v2/'"` and then upload it to your internal repository.

### Setting the Target Group

You will need to set a Target Group for the Deployment Step:

- Mouse-over the Deployment Step and click the `Edit` button.
    ![Editing a Deployment Step](/images/EditDeploymentStep.jpg)

- Navigate to the `Select Target Groups` panel.

- Highlight your preferred groups and click the `>` button to move them into `Selected Groups`.
    ![Selecting Target Groups](/images/SelectingTargetGroups.jpg)

- Click `Save`.

You are now ready to [move your Deployment Plan to Ready and run it](https://docs.chocolatey.org/en-us/central-management/usage/website/deployments#move-to-ready).