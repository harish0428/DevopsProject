# DevopsProject
This project is about building a scalable ans secure static web application in AWS to serve a basic 'helloworld' html page.
The steps involded are:
  1. Provisioned an ec2 instance in AWS with elastic loadbalancer, autoscaling group along with cloudwatch alarms to acieve more scalable      and secure application. This is written a single ansible module i.e., ec2_ubuntulaunch.yml 
  2. Used Ansible as a congiguration managemet tool. The main reason for choosing this is because of its agent-less architecture and easy      YAML language
  3. Wrote ansible playbook to install 'apache module' on host servers which includes site.yml and main.yml files
  4. site.yml is that file which gives information about hosts and varius roles such as webserver/appserver so on. In this project it          describes a single role i.e., websever
  5. main.yml is the main file where these roles are defined.It includes tasks, handelers and templates that are performed on webserver
  6. Template file defines the source of the html file which here indicates the helloworld.html file
 
 Finally, when the coomand 'ansible-playbook site.yml -i hosts' gets executed it finishes all the tasks that are mentione above and serves a static web page i.e., hello world message on the https port.
  
