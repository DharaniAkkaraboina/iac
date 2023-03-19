# PreReq 
Install Terraform locally
• Install Ansible locally
• Admin of an Azure subscription setup and ready to use.


## Test output
Build relevant secure network for 3 tiers. (Front end,backend and DB)
• Lock down access to front end to limited IP address
• Secure app.

## To use this code to create the network infrastructure with Terraform, follow these steps:
* Install Terraform: You need to install Terraform on your machine. 
- wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
- echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
- sudo apt update && sudo apt install terraform

## Create a Terraform project: 
clone this code main.tf all details wrote

## Initialize Terraform: 
Open a terminal or command prompt, navigate to the directory containing the main.tf file, and run the command terraform init. This will download and install the necessary providers for Azure.
-   terraform init.

## Authenticate with Azure: 
You need to authenticate with your Azure subscription to allow Terraform to create resources. You can do this by running the command az login and following the prompts.

## Test code
-  terraform plan

## Create the infrastructure: 
Run the command terraform apply to create the resources defined in your Terraform code. Terraform will prompt you to confirm that you want to create the resources. Review the changes and type "yes" to confirm.
-  terraform apply

## Verify the infrastructure: 
Once Terraform has finished creating the resources, you can verify that the network infrastructure has been created correctly by checking the Azure portal.

Note that this is just an example of how to create the network infrastructure with Terraform. You will need to customize the code to match your specific requirements and add additional resources, such as virtual machines and storage accounts, to complete the infrastructure for the three tiers. Additionally, you will need to use Ansible to configure the software on 
the virtual machines and secure the app.
