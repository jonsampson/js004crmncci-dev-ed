# Salesforce DevOps Center Trials

1) Install DevOps Center package in Developer Edition Org
2) Create this git repo from [this template](https://github.com/forcedotcom/dx-empty) provided by Salesforce
3) Create a new connected app in App Manager:
  - Connected App Name: DevOps Center
  - API Name: DevOps_Center
  - Contact Email: support@salesforce.com
  - Logo Image URL: https://tinyurl.com/doc-icon
  - Description: Manage your development and release processes
  - In Web App Settings, enter /sf_devops/DevOpsCenter.app as the Start URL.
  - Click “Save.”
  - In the Permissions Sets section, click “Manage Permission Sets.” If you’re viewing DevOps Center in the “Manage Connected Apps” page, click “Manage” to reach this page.
  - Select sf_devops_NamedCredentials, then click “Save.”
4) Set up own user to have permssion sets
  - assigned Dev Ops Center, DevOps Center Manager, DevOps Center Release Manager, sf_devops_InitializeEnvironments, sf_devops_NamedCredentials
5) Find the App DevOps Center in the app launcher menu
6) Create New Project and enter the Github authorization wizard. I allowed access to my personal account. We will probably have an Org set up to own this project.
7) Create New Project again and start actually configuring it. You select your production org as the destination and connect the pipeline up frome existing sandboxes (maybe scratch orgs?)
