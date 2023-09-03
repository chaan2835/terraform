siva git hub link https://github.com/techworldwithsiva

# terraform
terraform by shiva on roboshop

--------------------------

terraform installation on ubuntu

wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
----------------------------

for terraform we need to install aws cli2

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
apt install unzip
unzip awscliv2.zip
sudo ./aws/install
sudo ./aws/install --bin-dir /usr/local/bin --install-dir /usr/local/aws-cli --update
aws --version
----------------------------

we need to create a user in aws to work with terraform

1) go to iam
2) click on user and create a user (specify name) and click on next
3) click on attach polices directly and select admin access  and click on next then create user
4) once user is created click on that user and click on security creds and create access key
5) click on cli and mark the check-box then click on Next
6) go to the vm and setup the aws

        aws configure (provide the key)
