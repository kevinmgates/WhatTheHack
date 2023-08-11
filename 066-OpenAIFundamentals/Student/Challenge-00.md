# Challenge 00 - Prerequisites - Ready, Set, GO!

**[Home](../README.md)** - [Next Challenge >](./Challenge-01.md)

## Introduction

Thank you for participating in the OpenAIFundamentals What The Hack. Before you can hack, you will need to set up some prerequisites.

## Common Prerequisites

We have compiled a list of common tools and software that will come in handy to complete most What The Hack Azure-based hacks!

You might not need all of them for the hack you are participating in. However, if you work with Azure on a regular basis, these are all things you should consider having in your toolbox.

<!-- If you are editing this template manually, be aware that these links are only designed to work if this Markdown file is in the /xxx-HackName/Student/ folder of your hack. -->

- [Azure Subscription](../../../000-HowToHack/WTH-Common-Prerequisites.md#azure-subscription)
- [Managing Cloud Resources](../../../000-HowToHack/WTH-Common-Prerequisites.md#managing-cloud-resources)
  - [Azure Portal](../../../000-HowToHack/WTH-Common-Prerequisites.md#azure-portal)
  - [Azure CLI](../../../000-HowToHack/WTH-Common-Prerequisites.md#azure-cli)
- [Visual Studio Code](../../../000-HowToHack/WTH-Common-Prerequisites.md#visual-studio-code)
- [Azure Storage Explorer](../../../000-HowToHack/WTH-Common-Prerequisites.md#azure-storage-explorer)

## Description

Now that you have the common pre-requisites installed on your workstation, there are prerequisites specific to this hack. 

Please ensure that you have [Azure OpenAI access](https://aka.ms/oaiapply). This hack is self-paced and you will primarily be working with jupyter notebooks.

Please install these additional tools and resources:

- Python Installation, version at least \>= 3.6, the minimum requirement for using OpenAI's GPT-3.5-based models, such as ChatGPT.
  - [Python](https://www.python.org/downloads)
- Conda Installation, for project environment management and package management. Anaconda distribution is a popular Python distribution, while Miniconda is the lightweight version of Anaconda.
  - [Anaconda](https://docs.anaconda.com/anaconda/install) OR [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
- Environment setup:
  - Open Anaconda Prompt or your favourite terminal and verify Python and Conda installations using `python --version` and `conda --version`
  - Create a project environment using Conda - `conda create --name <env_name>`
  - Activate Conda environment - `conda activate <env_name>`
  - Install the required libraries listed in the requirements.txt file via `pip install -r requirements.txt`
  - Open the project in VS Code using `code .`
- [Create an Azure OpenAI Resource](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/overview) 
- Deploy the following models in your Azure OpenAI resource. A couple of challenges may require a few additional prerequisites so be sure to checkout the pre-reqs for the respective challenges. 
  - `gpt-35-turbo`
  - `text-davinci-003`
  - `text-embedding-ada-002`
- Add required credentials of Azure resources in the `.env` file
  - **NOTE:** Additional Azure resources such as Azure Form Recognizer and Azure Cognitive Search will be required for later challenges. Make sure to update ``.env`` file with credentials as needed. 

## Success Criteria

To complete this challenge successfully, you should be able to:

- Verify that you have Python and Conda installed.
- Verify that you can run Jupyter Notebooks in Visual Studio Code.
- Verify that you have created the AOAI resource and deployed the necessary deployments.
