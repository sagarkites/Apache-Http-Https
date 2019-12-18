# Apache httpd-https in Ec2-instance 
* get the Instance-details amd-id, subnet-id, sg-id, and name of key-pair that you crreated
* Run the playbook - ansible-playbook instance.yml
* dynamic inventory - get the aws api responses dynamically with respect to Regions 
* chmod 755 ec2.py 
* ./ec2.py --list - gets the all respones grab the ip 
* grab ip or dns of instance - ansible -i ec2.py us-east-1 -u <user> -m ec2_ec2_instance_facts  
* Playbook - ansible-playbook <playbook> -i ec2.py -u <user> -l ip 
    - make sure that in playbook has host: all
    - roles-stucture 
    - tasks - main.yml
    - files - .conf, html file 
    - handlers - main.yml
* apache ssl and virtual host configuration file 
    - make sure custom module mod_ssl was present 
    - copy the keys to the ssl.conf
    - to redirect http to https - Redirect permenent / https://<dns of instance>
