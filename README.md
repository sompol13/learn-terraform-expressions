## Learn Terraform Expressions
In this tutorial, you will deploy a pre-generated webapp to EC2 instances behind an ELB. You will:
* use `locals` to assign your expressions to variables for reuse.
* use conditionals to declare if you want your configuration to contain multiple instances for high-availability.
* use the `splat` expression to return multiple private IPs in your network.

### Name expressions with locals
- Update the network resources of your configuration and add the `local.common_tags` expression to your `tags` attribute.
- Create a new file called `outputs.tf` and add the values for your instance tags.
- `terraform init`
- `terraform apply`

### Create a conditional for your locals criteria
Your `local` block accepts conditional criteria. Update your `main.tf` file with new criteria. If the `name` variable is blank, the output of the `random_id` resource is the tag value.

### Create a conditional count criteria
Open `variables.tf` and add a new boolean variable for high availability.

### Update your instance configuration
Open `main.tf` in your editor and update your aws_instance count parameter with the new conditional variable criteria. 

### Create a splat expression
Edit the `outputs.tf` file to add the new private_addresses output. This output will return the private DNS of all instances created by the `aws_instance.ubuntu` resource.

### Reference
https://learn.hashicorp.com/tutorials/terraform/expressions