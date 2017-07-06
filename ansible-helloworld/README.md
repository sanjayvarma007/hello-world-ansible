The following project is used to successfully deploy the hello world index.html page on to apache webserver using aws ec2 and s3 resources.
The aws resources are deployed using ANSIBLE.
We implement IAC IT infrastructure using configuration management tool like ANSIBLE and its huge libraries of modules to completely avoid the usage of aws console.
For fully maintaining the lifecycle and security of the instances. I created three playbooks which perform the below addressed tasks.

1) create-ec2-instance.yml playbook will spin up a new ec2 instance. The variables within the yaml file can be tweaked to provision different instances with different ami images, secuirty groups etc
(we need to input the access id and secret id while executing the playbook)

2) terminate-ec2-instance.yml will terminate the selected instances without using the aws console
we need to input the accessid and secret id with the instance id to terminate that particular instance

3) create-securitygroup.yml will create security group within ec2 instance dashboard
we need to input the accessid and secret id. The VPC can be changed from default to private if necessary

Example:
ADHOC command
ansible-playbook playbooks/terminate-ec2-instance.yml --extra-vars="instanceid=.... accessid=... secretid=.... "

The projects desired outputs can be found within the outputs subdirectory
