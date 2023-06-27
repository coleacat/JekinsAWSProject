# Using Terraform to Deploy a Jenkins Server on AWS 

This project was created from this [tutorial.](https://www.freecodecamp.org/news/learn-terraform-by-deploying-jenkins-server-on-aws/)

It is still a work in progress and future updates will make this a more personalized project.

## Installing Terraform on Windows
* Install [Chocolately](https://chocolatey.org/install#individual) package manager.
* Install the Terraform package from the command-line.
```properties
 choco install terraform
```
* Verify the installation was completed successfully
```properties
terraform -v
```

## Useful Terraform commands
### Initialize your Terraform working directory
- ```terraform init``` #initialize directory

### Format and Validate Terraform code
- ```terraform fmt``` #format code per HCL standard
- ```terraform validate``` #validate code for syntax

### Plan, Deploy and Cleanup Infrastructure
- ```terraform apply``` #apply deployment changes 
- ```terraform destroy``` #destroy/cleanup deployment
- ```terraform plan``` #output the deployment plan to plan.out
- ```terraform apply -target=aws_instance.my_ec2``` #only apply/deploy changes to the targeted resource
-```terraform <apply/plan> -var-file="secrets.tfvars"``` #specify the tfvars file that should be used
- ```terraform <apply/destroy> --auto-approve``` #/destroy changes without being prompted to enter “yes”
- ```terraform refresh``` #reconcile the state in Terraform state file with real-world resources
- ```terraform providers``` #get information about providers used in current configuration

### Terraform State Manipulation
- ```terraform state show aws_instance.my_ec2``` #show details stored in Terraform state for the resource
- ```terraform state list``` #list out all the resources tracked via the current state file

This is a pull-request-test