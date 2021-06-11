## Install the Azure CLI
Install the the Azure CLI in one step like so: `curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash`{{execute}}

## Install the Azure Machine Learning CLI
Clone the example repository with the command `az extension add -n ml`{{execute}}

Run the help command to make sure the install worked `az ml -h`{{execute}}

## Log into Azure
Let's log into Azure and set some defaults `az login`{{execute}}
then set the default subscription `az account set -s "<YOUR_SUBSCRIPTION_NAME_OR_ID>"`{{execute}}
optionally creata a new resource group `az group create -n "azureml-examples-rg" -l "eastus"`{{execute}}
then set your default resource group and workspace `az configure --defaults group="azureml-examples-rg" workspace="main"`{{execute}}



## Clone Example Files

Clone the example repository with the command `git clone https://github.com/Azure/azureml-examples --depth 1 && cd azureml-examples/cli/jobs`{{execute}}

Let's look at a simple AML job definition `/azureml-examples/cli/jobs/hello-world.yml`{{open}}.

And then let's run the sample `az ml job create -f hello-world.yml --web --stream`{{execute}}

