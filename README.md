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
---------------------------------

advantages
1) version control:

    since it is code, we can maintaion code in git. we can completely maintain
    the history of infra and the collabration is easy.

2) consistent infra:

    often we face the problem of different configurations in diff envs like
    dev,test,prod using terraform we can create the same infra inf multiple
    envs with more reliability.

3) Automated infra (CRUD-create,read,update,delete):

    using terraform we can create entire infra in minutes without human errors.
    updating infra using terraform is easy.
    using terraform we can delete infra.

4) Inventory management:

    If we create infra manually it is tough to maintain inventory resouces in
    diff regions. But by seeing terraform you can easily tell the resources
    you are using in diff regions.

5) cost optimisation:

    when we need infra we can create in minutes. when we don't need we can delete in minutes.
    so we can save the cost.

6) Automatic dependency management:

    terraform can understand the dependency of resources. It can tell us the dependency clearly.

7) modular infra:

    code resue. we can develop our own modules to reuse the infra code.
    instead of spending more time to create infra from the sctrach we can reuse the modules.