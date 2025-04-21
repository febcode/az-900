Exercise - Create an Azure virtual machine
Completed
100 XP
10 minutes
Sandbox activated! Time remaining: 
You have used 1 of 10 sandboxes for today. More sandboxes will be available tomorrow.

In this exercise, you create an Azure virtual machine (VM) and install Nginx, a popular web server.

You could use the Azure portal, the Azure CLI, Azure PowerShell, or an Azure Resource Manager (ARM) template.

In this instance, you're going to use the Azure CLI.

Task 1: Create a Linux virtual machine and install Nginx
Use the following Azure CLI commands to create a Linux VM and install Nginx. After your VM is created, you'll use the Custom Script Extension to install Nginx. The Custom Script Extension is an easy way to download and run scripts on your Azure VMs. It's just one of the many ways you can configure the system after your VM is up and running.

From Cloud Shell, run the following az vm create command to create a Linux VM:

Azure CLI

Copy
az vm create \
  --resource-group "learn-1382b4f7-8311-46a6-9db0-506400b0f0ed" \
  --name my-vm \
  --public-ip-sku Standard \
  --image Ubuntu2204 \
  --admin-username azureuser \
  --generate-ssh-keys    













Your VM takes a few moments to come up. You named the VM my-vm. You use this name to refer to the VM in later steps.

Run the following az vm extension set command to configure Nginx on your VM:

Azure CLI

Copy
az vm extension set \
  --resource-group "learn-1382b4f7-8311-46a6-9db0-506400b0f0ed" \
  --vm-name my-vm \
  --name customScript \
  --publisher Microsoft.Azure.Extensions \
  --version 2.1 \
  --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' \
  --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'    













This command uses the Custom Script Extension to run a Bash script on your VM. The script is stored on GitHub. While the command runs, you can choose to examine the Bash script from a separate browser tab. To summarize, the script:

Runs apt-get update to download the latest package information from the internet. This step helps ensure that the next command can locate the latest version of the Nginx package.
Installs Nginx.
Sets the home page, /var/www/html/index.html, to print a welcome message that includes your VM's host name.
Continue
This exercise is complete for now. The sandbox keeps running, and you come back to this point in a few units to update the network configuration so you can get to the website.
138.91.184.93