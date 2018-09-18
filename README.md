# What is Jenkins? 
Jenkins is an open source automation server written in Java. Jenkins helps to automate the non-human part of the software development process, with continuous integration and facilitating technical aspects of continuous delivery.


## Jenkins install with Ansible
Thank you for reading documentation before run any command after cloning this repository. Please run the following command
```
git clone https://github.com/farkhodsadykov/Jenkins-Ansible.git
cd Jenkins-Ansible
```


## Crate Droplet on Digital Ocean.
This step will create a droplet on DigitalOcean. Make sure you have already token from DigitalOcean. If you don't know how to get follow  the [link](https://www.digitalocean.com/community/tutorials/how-to-create-a-digitalocean-space-and-api-key). 
If you have already installed remote machine skip these two command:
``` 
source VENV/bin/activate # activate Virtual ENV
python createDroplet.py
```


## Run the Ansible Playbook 
Make sure you have ssh key on remote system 🔐. if you have ssh key as root run
```
ansible-playbook -u root -i hosts install-jenkins.yml
```
if you have different user, make sure you have that user inside `visudo`then run:
```
ansible-playbook -u yourusername -i hosts install-jenkins.yml
```




