# WebAPI
WebAPI Framework4.8 and setup CI/CD in the Azure Devops

## Add the resource and deployment the WebAPI on local
+ Create an account in the Azure Devops
+ Create an environment in the Azure Devops(Ex: `Test` and add tag name server `web-api`)
+ Add the resource in the environment
    - Select `Virtual Machine`
    - Copy a command line(register script) which show in a popup in the Azure Devops after click `Add the resource`
    - Paste the command in the powershell on the local(this my PC)
+ Create a github repo
+ Create an azure-pipeline.yml for building and deployment the App on IIS in thelocal
    - Trigger the master branch
    - Build WebAPI
    - Archive zip and unzip files
    - Create virtual app on the local machine
    - Deploy a virtual app on the local machine

+ Build azure pipeline on the local with `webapi` virtual app
    - Navigate to `http://localhost/webapi/api/values/`