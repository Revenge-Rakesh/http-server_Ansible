# http-server_Ansible
#Deploy HTTP- Server Service Using Ansible

Aim: This Repository will help to deploy the Http service Using the Ansible and Docker

- This repo contains the three major files.
  1. Inventory and all.yml
  2. docker-compose.yml
  
  
- Inventory will tell you, where our application needs to be deployed. 
  i.e. On which server with which user, Ip of server and User.
- All.yml file will have the external parameters we want to use.
  Such as deployment path of application and application user.
- We can combine both all.yml and inventory file, if we want.


#Steps to Deploy

1. Clone the repo and Fill the all.yml and Inventory file as per the requirememt.
2. Create the connectivity from the server where the repo is there to the server where you want to deploy the application.
   Example:  ssh <application_user>@<ip_of_server_where_the_application_is_deploed>
3. Run the Below ansible tag to deploy the service.

ansible-playbook deploy.yml -i inventory --tags http

if you have pem file to login to the server use the below ansible command.

ansible-playbook deploy.yml -i inventory --tags http --private-key <pem_file_path>
