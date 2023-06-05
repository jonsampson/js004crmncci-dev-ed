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
8) Create org shape of developer edition `sfdx force:org:shape:create -u js004@js004crmncci.sandbox.dev`
9) Create dev environment scratch org - `sfdx force:org:create -f config/devcenter-enabled-scratch-def --durationdays 30`
10) Open scratch org `sfdx force:org:open -u xx@example.com`
11) Set a password for the scratch org user `sfdx force:user:password:generate --targetusername xx@example.com`
12) Go back to DevOps Center and chose this as the intregration environment.
13) Go to 9 until the rest of the envs are populated
  - a developer edition can only have 3 scratch orgs
14) Activate the Pipeline
15) Create a Work Item
