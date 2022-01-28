## Learn Terraform Expressions
In this tutorial, you will deploy a pre-generated webapp to EC2 instances behind an ELB. You will:
* use `locals` to assign your expressions to variables for reuse.
* use conditionals to declare if you want your configuration to contain multiple instances for high-availability.
* use the `splat` expression to return multiple private IPs in your network.

## Name expressions with locals
- Update the network resources of your configuration and add the `local.common_tags` expression to your `tags` attribute.
- Create a new file called `outputs.tf` and add the values for your instance tags.
- `terraform init`
- `terraform apply`

### Reference
https://learn.hashicorp.com/tutorials/terraform/expressions