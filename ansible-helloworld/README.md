The following project contains three playbooks which are used to successfully deploy the hello world html page.

1) create-ec2-instance.yml will spin up a new ec2 instance
we need to input the access id and secret id while executing the playbook

 
2) terminate-ec2-instance.yml will terminate the selected instances
we need to input the accessid and secret id with the instance id to terminate that particular instance

3) create-securitygroup.yml will create security group within ec2 instance dashboard
we need to input the accessid and secret id. The VPC can be changed from default to private if necessary

Example:

ansible-playbook playbooks/terminate-ec2-instance.yml --extra-vars="instanceid=.... accessid=... secretid=.... "
