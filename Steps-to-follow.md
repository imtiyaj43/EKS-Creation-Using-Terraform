## Step 0: Launch a New Ubuntu EC2 Instance (t2.micro) and Install Terraform

1. Launch an Ubuntu EC2 instance of type t2.micro on AWS.
2. Install Terraform on this instance by following the appropriate steps after logging in to your EC2 server.

## Step 1 : Install AWS CLI latest version
```
sudo apt install unzip
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
aws --version
```
### Run the following command to configure your AWS CLI:
```
aws configure
```
### You will be prompted to enter:
   - Access Key: Enter your AWS Access Key.
   - Secret Access Key: Enter your AWS Secret Access Key.
   - Region: Choose the region you want to use (e.g., us-west-2).
   
   Ensure you enter the details correctly to allow AWS CLI to interact with your AWS resources.


## Step 2 : Install Kubectl latest version using below commands
```
curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.19.6/2021-01-05/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin
kubectl version --short --client
```
### After succefully installting all the above packages execute terraform commands.
