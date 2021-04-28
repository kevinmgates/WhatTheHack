# What The Hack: DevOps with GitHub 

## Challenge 6 – Continuous Delivery (CD)

[< Previous](challenge05.md) - [Home](../readme.md) - [Next >](challenge07.md)

### Introduction

In DevOps after we automate our build process, we want to automate our release process, we do this with a technique called Continuous Delivery (CD). Please take a moment to review this brief article talking about why this is important. 

- [What is Continuous Delivery?](https://docs.microsoft.com/en-us/azure/devops/learn/what-is-continuous-delivery)

### Challenge

In this challenge, we will use GitHub Actions to deploy our container image to the dev environment. 

**OPTIONAL**: Use your code editor (VS Code) to update your workflow file locally on your machine. Remember to commit and push any changes.

Extend the workflow you created in Challenge #5:
1. Create a new job. Make sure it doesn't run until the previous jobs complete.

2. Configure your `dev` environment (App Service) to pull the latest container image from ACR. 
   - Login to Azure using your service principal, if needed ([hint](https://docs.microsoft.com/en-us/azure/app-service/deploy-container-github-action?tabs=service-principal#tabpanel_CeZOj-G++Q-3_service-principal))
   - Use the `Azure/webapps-deploy@v2` [action](https://github.com/Azure/webapps-deploy) to update the Web App to pull the latest image from ACR. Key parameters to configure:
      - `app-name` - the name of the wep app instance to target
      - `images` - the path to the image you pushed to ACR

3. Make a small change to your application  (i.e.,`Application/src/RazorPagesTestSample/Pages/Index.cshtml`), commit, push, monitor the workflow and see if the change shows up on the dev instance of the website.

4. Update the workflow to deploy the app to the `test` environment (App Service) - but *only* after a manual approval.

### Success Criteria

1. A small change to `Application/src/RazorPagesTestSample/Pages/Index.cshtml` automatically shows up on the website running in the dev environment (i.e., `<prefix>devops-dev`.azurewebsites.net).
2. After the app is deployed and validated in `dev`, there is a manual approval step and then the app is deployed to the `test` environment.

### Learning Resources

- [Deploy a custom container to App Service using GitHub Actions](https://docs.microsoft.com/en-us/azure/app-service/deploy-container-github-action?tabs=service-principal#tabpanel_CeZOj-G++Q-3_service-principal)
- [Approval workflow for GitHub Actions](https://timheuer.com/blog/add-approval-workflow-to-github-actions/)
- [Workflow syntax for environments](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idenvironment)
- [Environment protection rules](https://docs.github.com/en/github-ae@latest/actions/reference/environments#environment-protection-rules)

### Advanced Challenges (optional)

1. Update the workflow to deploy the app to the `prod` environment *after* it is deployed to the test environment - but *only* after a manual approval.

[< Previous](challenge05.md) - [Home](../readme.md) - [Next >](challenge07.md)
