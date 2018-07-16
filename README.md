# ansible-aws
ansible aws project

## Configuration on control host
- Download ec2.py
https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.py
  - Setup executable permissions to ec2.py
```
chmod u+x ec2.py
```
- Download ec2.ini
https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.ini
- Update .bash_profile
AWS_REGION="ap-southeast-1"
export AWS_REGION
ANSIBLE_HOSTS=/root/aws_work/ansible-aws/ec2.py
export ANSIBLE_HOSTS
ANSIBLE_INVENTORY=/root/aws_work/ansible-aws/ec2.py
export ANSIBLE_INVENTORY
EC2_INI_PATH=/root/aws_work/ansible-aws/ec2.ini
export EC2_INI_PATH
- Download EC2 ssh key and copy to /root/.ssh
  - for example: sing_keypair4.pem

## Provision EC2 CCI
- Mandatory parameters: ec2_operation=launch_instance, instance_name=a useful tag for name of instance
```
ansible-playbook /root/aws_work/ansible-aws/ec2_site.yml -e ec2_operation=launch_instance -e instance_name=Springboot_Test1
```

## De-provision EC2 CCI
- Mandatory parameters: ec2_operation=release_instance, instance_name=Tag given at instance creation
```
ansible-playbook /root/aws_work/ansible-aws/ec2_site.yml -e ec2_operation=release_instance -e instance_name=Springboot_Test1
```


