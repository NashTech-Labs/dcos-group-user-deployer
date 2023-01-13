### What will this role do ?

The above deployer role will create group and user deployer and further will create the sudo user as per the permission.

First the group deployer will be created and then the user deployer created will be deployed to that group.
In the next step the role will create ssh folder under the deployer owner and group. Then the user will be granted with the sudoer permission.

**NOTE** : The above role helps in DCOS infrastructure for deployer group and user creation.


#### Terms  used in the role.

- master , slave , captain :  These are the nodes of dcos infrastructure and  
                           
                           you can  give names of your node as per your infra. 
                           
- deployer:   This is the default user that will be used for deploying apps in dcos. 



### How to run the playbook .

To run the playbook follow the below command:-

`ansible-playbook -i <your inventory file> playbook.yml`

**Note**:-  If you are running on your local system then you don't need to pass inventory file. Just use localhost in hosts of playbook. 