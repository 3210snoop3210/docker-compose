# docker-compose
For docker compose tests task
1) Configuring on AWS EC2 instance on Red Hat family 9 ami (RHEL-9.4.0_HVM-20240605-x86_64-82-Hourly2-GP3) with creating key-pair for usage via SSH from localhost and later for ansible using somehowe command, like this: ssh ec2-user@some_public_ip_or_dns_name_of_instance -i .some_created_in_aws_key_pair.pem
   
2) Create docker compose file and test it locally on EC2 instance and file with ENV variablse
   1 image with latest mysql  for mysql (we provisioned volumes and networks for future connections btw images) and 1 with adminer as web-server and forwarding port 8080
   
3) Create Ansible playbook file with some description in playbook which I duplicate here:
   # Change hostname
   # Set timezone to Kyiv
   # Create Docker user
   # Add docker Centos repos
   # Install Docker , Docker Compose and dependencies
   # Configure Docker user to use Docker without sudo
   # Open ports 22, 80, and 443
   # Reload firewall to apply changes
   # Clone Docker Compose repository
   # Run Docker Compose file
   # Enable Docker Compose to start on boot

4) I was create public repo in my github account with all files:
https://github.com/3210snoop3210/docker-compose.git
5) Run ansible playbook from Virtualbox Linus Virtual machine ansible to setup all steps
6) Please, check all in remove host to remove from my side from AWS
