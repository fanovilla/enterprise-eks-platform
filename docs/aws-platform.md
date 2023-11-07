

# account-factory for terraform

* control tower
* account factory for terraform
  * create aft account clickops
  * auth to org-mgmt account via github oidc <org>/aws01-aft - manual CloudFormation
  * manual workflow


# AWS Identity Center with Azure AD 



topology


https://docs.aws.amazon.com/whitepapers/latest/organizing-your-aws-environment/organizing-your-aws-environment.html


multiple org
https://docs.aws.amazon.com/whitepapers/latest/organizing-your-aws-environment/multiple-organizations.html#test-changes-to-your-overall-aws-environment

"test" organization

Test changes to your overall AWS environment

You might need to develop code that interacts with APIs and other mechanisms fundamental to the management of your 
organization. In these cases, to determine whether your changes break something without having to make the changes in 
your production organization, we recommend that you test your changes in an organization different from the one running 
your production workloads.

For example, you might need to either modify the automation that creates new accounts to change the configuration 
baseline of accounts it creates or change the configuration of a workflow management system you're using to modify SCPs. 
In addition, you might want to test the delegated administration capabilities of various AWS services prior to applying 
them in your production organization.

In these circumstances, we recommend that you establish an additional organization for testing that resembles your more 
formally managed production organization. You can perform testing of changes to how you manage your organization in your 
test organization before applying those changes to be applied to your production organization.

main organization

https://aws.amazon.com/blogs/networking-and-content-delivery/ip-address-management-for-aws-control-tower/





# accelerators

https://github.com/aws-samples/aws-secure-environment-accelerator

https://aws.amazon.com/solutions/implementations/landing-zone-accelerator-on-aws/