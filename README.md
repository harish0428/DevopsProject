# DevopsProject
This project is about building a scalable and secure static web application in AWS to serve a basic 'helloworld' html page.
The steps involded are:
  1. Provisioning an ec2 instance in AWS with elastic loadbalancer, autoscaling group along with cloudwatch alarms to achieve more              scalable and secure application. This is written using a single ansible module (ec2_ubuntulaunch.yml) 
  2. Using Ansible as a configuration management tool. The main reason for choosing is because of its agent-less architecture and              easily comprehendible YAML language
  3. Writing ansible playbook to install 'apache module' on host servers(which in this case is a web server)  also includes site.yml and        main.yml files
  4. site.yml is the file which gives information about hosts and various roles such as webserver/appserver so on. In this project it          describes a single role websever
  5. main.yml is the main file where these roles are defined.It includes tasks, handlers and templates that are performed on webserver
  6. Hosts file has the information about the servers fully qualified domain name (I have left it generic). We could add in the FQDN as        per need
  6. Template file defines the source of the html file which here indicates the helloworld.html file
 
 Finally, when the command 'ansible-playbook site.yml -i hosts' gets executed it finishes all the tasks that are mentione above and serves a static web page i.e., hello world message on the https port.
  
