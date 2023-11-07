# Organization Topology

This [solution overview](https://aws.amazon.com/blogs/networking-and-content-delivery/ip-address-management-for-aws-control-tower/#attachment_12834) 
shows a multi-organization topology with these names:
* Main Organization
* LOB Organization - 1
* LOB Organization - 2

And this [guide](https://docs.aws.amazon.com/whitepapers/latest/organizing-your-aws-environment/multiple-organizations.html#test-changes-to-your-overall-aws-environment) 
mentions the use of a `test organization` to test platform changes against before applying to your main organization.

Thus, as a minimum, we aim to build these 2 organizations:
* main organization - to host workloads (all nonprod and prod environments), fully fleshed out org structure
* test organization - for sole use by the platform team to test changes

# Setting up AWS Control Tower

Following the user guide at https://docs.aws.amazon.com/controltower/latest/userguide/setting-up.html

## Sign up for an AWS account

This initial account will be the organization management account.
See https://docs.aws.amazon.com/organizations/latest/userguide/orgs_best-practices_mgmt-acct.html

Information guidelines - https://docs.aws.amazon.com/SetUp/latest/UserGuide/setup-acctrequirements.html

Example suggested naming standard: `organization-purpose-environment`

* Root user email address - use a corporate distribution list; 
  for personal POC the gmail 'plus addressing' trick is useful - ex. `me+awsmain-mgmt-prod@gmail.com` 
* AWS account name - `awsmain-mgmt-prod`

## Create an administrative user

* Turn on multi-factor authentication (MFA) for your root user
* Enable IAM Identity Center - https://docs.aws.amazon.com/singlesignon/latest/userguide/get-started-enable-identity-center.html#get-started-enable-identity-center-sign-in-enable
  * default identity source will be `Identity Center directory`
  * take note of the generated AWS access portal URL
* Add user
  * Username - `admin`
  * Email address - use a corporate distribution list; POC ex. `me+awsmain-admin@gmail.com`