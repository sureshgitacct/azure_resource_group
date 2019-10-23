# Azure Resource Group
This will create an Azure Resource Group. The user must provide a valid location (i.e. East US)

You can apply a policy to the region. The following has already been added to the scalr-module.hcl:

```
version = "v1"

variable "region" {
  policy = "cloud.locations"
  conditions = {
  cloud = "azure"
  }
}
```

Now all you have to do is create a Cloud.Locations policy at the account level and assign the policy to your environment. See more here: https://scalr-athena.readthedocs-hosted.com/en/latest/catalog/variables.html#binding-to-policy

See this Terraform template here: https://github.com/scalr-eap/azure_resource_group
