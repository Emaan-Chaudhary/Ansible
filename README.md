# Ansible Webpage Deployment

This repository contains **Ansible playbooks** to automatically deploy a static website using **Nginx** on remote servers.  

---

## **Project Overview**

- Install Nginx on the remote server(s).  
- Start and enable Nginx service.  
- Deploy a custom `index.html` webpage to `/var/www/html`.  

This setup allows you to **quickly deploy a static website** on multiple servers with minimal manual work.

---

## **Prerequisites**

- Remote servers running Ubuntu/Debian.  
- SSH access to remote servers.  
- Ansible installed on the control machine.  
- Your `index.html` file ready in the playbooks directory.

---

## **Inventory Setup**

Example `inventory` file:

```ini
[prod]
server-1 ansible_host=<server_ip>

[all:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=~/keys/shell-key.pem
ansible_python_interpreter=/usr/bin/python3
