# WebAPI
- WebAPI Framework4.8 and setup CI/CD in the Azure DevOps
- Using azure pipeline for build and deployment the WebAPI on locally
- Connected the source code from Github

## Add the resource and deployment the WebAPI on local
+ Create an account in the Azure DevOps
+ Create an project in the Azure DevOps
+ Create an environment in the project of the Azure DevOps(Ex: `Test` and add tag name server `web-api`)
+ Add the resource in the environment
    - Select `Virtual Machine`
    - Copy a command line(register script) which show in a popup in the Azure DevOps after click `Add the resource`
    - Paste the command in the powershell on the local(this my PC)
+ Create a github repo and connect with the project in the project settings
+ Create an azure-pipeline.yml for building and deployment the App on IIS in thelocal
    - Trigger the main branch from Github
    - Build WebAPI
    - Archive zip and unzip
    - FileTransform: this add environment variables from Group variables and Variables from yml file if any
    - Create virtual app on the local machine
    - Deploy a virtual app on the local machine

+ Build azure pipeline on the local with `webapi` virtual app
    - Navigate to `http://localhost/webapi/api/values/`
