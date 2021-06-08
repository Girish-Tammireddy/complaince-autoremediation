# AWS-Config-compliance-monitoring and autoremediation
Deployment overview

 Step. 1 Launch the stack

    Launch the AWS CloudFormation template into your AWS account.

Step. 2 Configure service catalog portfolio permissions

    Grant access to IAM users.

Step. 3 Deploy the playbook(s)

    Install or upgrade CIS or AFSB playbooks.


Step 1. Launch the AWS cloudformation stack :
Sign in to the AWS Management Console from the account where the AWS Security Hub is currently configured, and launch the aws-sharr-deploy.template AWS CloudFormation template. 

Step 2. Configure service catalog portfolio permissions
 To grant access to IAM users, do one of the following:
    Add IAM users, roles, or groups to the AWS Service Catalog portfolio
    
Step 3: Deploy the playbook(s)
 From the Security Hub Admin account, navigate to the AWS Service Catalog
and choose CIS.

Choose Launch Product.

Enter a name for the instance. For example, CIS-v-1-2-0.

Choose the latest version.

Choose Next.

On the Parameters page, each individual remediation has the option to be invoked automatically when a matching Amazon CloudWatch Logs event occurs for the finding. **Note: The remediations cannot be automatically undone. By default, the automatic initiation is turned off for all remediations. Make your selections and then choose Next.


Optional step:

In case if you want to manage this solution across the accounts :

Select the  CISPermissions.template AWS CloudFormation template and then deploy it to the secondary accounts.
You can either use AWS CloudFormation StackSets, or manually sign in to each account and then deploy the permissions template. 



