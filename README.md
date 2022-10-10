# checkov-terraform
Checkov Terraform code


curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
az login --use-device-code
az account set --subscription="54d87296-b91a-47cd-93dd-955bd57b3e9a"
az group show --name RG_TerraformLab_20221010

wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform

terraform plan -out main.tfplan
docker run -it centos:centos8 /bin/bash
docker run -it -v /workspace/checkov-terraform/code:/root centos:centos8 /bin/bash

dnf module -y install python38
python3 -V
pip3 install checkov