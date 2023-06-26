# roboshop-ansible

##Ansible supports push and pull
##Ansible uses ssh conection
##Ansible uses some inventory file
## The same script that we kept in a file for bash script is the same script that we will provide in ansible
#playbook and the play book should be written in a mark up languange

##Ansible play book is written in keys and value pair
#Mark up language are written in 3 format Plain. List and  Map/dictionary

Yaml is simple key value map
In yaml indentation is very key

#Example of plain
## a: = 10

#Examples of list
## b: [ 99,89 ]
## b: 
#  - 99
#  - 89

#Examples of Map
# c:
  course: DevOps
  time: 730am

# c: { Course: DevOps,
# time: 7:30am }

# Ansible is expecting the inputs in yaml 
# keys are provided by ansible and we need to refer to the documentation 
# keys are called parameters and provided by ansible
# some values are also provided by ansible
# Ansible will provide the keys and the value and you tell ansible what you want to do 
# If you are installing a package you have to tell ansible what package you are installing
# You have to open the documentation , read it understand and implement it

# How to write a playbook
name: Some Playbook
hosts: all
tasks:
  - name: Demo Tasks
    ansible.builtin.yum:
      name: nginx
      state: installed

 - name: Some role play
   hosts: all
   roles:
     - demo


# The name is a key word provided by ansible and we are giving our value some playbook
# hosts is a key word provided by ansible and we give our value all
# tasks is a key word provided by ansible
# We provide the name (demo task) and module (ansible.builtin.yum)
# name (nginx) provided by ansible
# state (installed) provided by ansible

# file extension can be .yml or .yaml

## sample.yaml is a playbook
   every playbook starts with a list with a hyphen and it can have one or more plays
   name keyword on play is optional and good to have 
   The hosts is must to have, that is which hosts to connect
   Either task/roles is a must to have role 


Install Ansible   


##In the workstation server - sudo labauto ansible

YAML
1. Indentation is the way of YAML inputs provided
2. Always use uniform spacing
3. Tab space are not allowed
4. Based on the program you are dealing, keys are provided by program and we have to fill those values as per our requirements
5. same cases we create our own keys mainly variables
6. some cases the values also will be provided and we have to choose only one of them