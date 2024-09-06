# Ansible-Playbook
# Anaible&Vagrant project




# Prerequisite

1: Oracle VM Virtualbox

2: ansible

3: Vagrant



# Project Overview

This project involves automating the deployment of a web application using Vagrant and Ansible. The setup includes provisioning five virtual machines (VMs) to handle different components of the application. The VMs are configured as follows:

    Tomcat VM: Hosts the Apache Tomcat application server.
    NGINX VM: Acts as a reverse proxy server using NGINX.
    MariaDB VM: Provides the MariaDB database service.
    RabbitMQ VM: Manages message queuing with RabbitMQ.
    Memcached VM: Utilizes Memcached for caching.

The Vagrant configuration manages VM provisioning, while Ansible handles the configuration and deployment of the software on each VM. This setup allows for scalable and efficient deployment of web applications.

# Project steps 

Create an Ansible playbook for each VM 

# ansible-db.yml

![image](https://github.com/user-attachments/assets/22669ed1-16b0-4814-8ecb-4ee0f2d6edd8)

![image](https://github.com/user-attachments/assets/ccd6926f-7ff2-40cf-9163-803563282290)

![image](https://github.com/user-attachments/assets/e81d64ba-f152-4eee-a2ca-a36755540bd4)

![image](https://github.com/user-attachments/assets/345fb471-c897-40e2-a214-3b06f83dbe04)

# ansible-mc.yml

![image](https://github.com/user-attachments/assets/5130487b-b85b-44a9-ae6b-ef57b385290f)

![image](https://github.com/user-attachments/assets/74b25ba5-0a82-4c7a-abb3-9e781c8bcc5d)


# ansible-rmq.yml

![image](https://github.com/user-attachments/assets/8422d6a3-a354-42e3-9389-1944b9545c57)

![image](https://github.com/user-attachments/assets/9a8f8036-09cd-4109-a933-3ca76ca7e4c1)

![image](https://github.com/user-attachments/assets/fadb7c77-8bf0-4855-91ea-800c8d1afd41)


# ansible-app.yml

![image](https://github.com/user-attachments/assets/0ecafb0a-ec1a-412d-bbce-feb455f368a2)

![image](https://github.com/user-attachments/assets/74585aac-35d4-49f7-b230-c09613eecab7)


![image](https://github.com/user-attachments/assets/f82505a3-118f-4d6a-bb03-af0c672a3d9e)

![image](https://github.com/user-attachments/assets/ddb46765-c774-428f-bf7b-22a114330654)


# ansible-web.yml

![image](https://github.com/user-attachments/assets/2a475ac4-1b99-42b3-ac93-a2e16a0e0950)

![image](https://github.com/user-attachments/assets/36d74eb1-03c5-4d56-a447-0b998fa6b91d)

# After Creating Ansible Playbooks we will Create a Vagrantfile

# Vagrantfile

![image](https://github.com/user-attachments/assets/fac0335d-e637-4536-906f-78a2608a7677)


![image](https://github.com/user-attachments/assets/d88cd099-d882-49a0-82b0-eafec47f1966)

![image](https://github.com/user-attachments/assets/b157d709-2aba-48cd-ac70-8e414455488e)


# And after creation write in the terminal vagrant up 

![image](https://github.com/user-attachments/assets/c8492b0b-8be8-4dab-ab63-c1bed9b47960)

![image](https://github.com/user-attachments/assets/ba573805-460b-4971-8736-c43c4a3b9168)

![image](https://github.com/user-attachments/assets/91ee245e-dc2a-4429-b0c9-654cc54352ca)

