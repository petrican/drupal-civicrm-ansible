# drupal-civicrm-ansible
Drupal - CiviCRM Ansible Demo installation to AWS

Automated Drupal and CiviCRM secure cloud installation with SSL certificate using https://letsencrypt.org/

Automates the creation of a new server with Drupal 7 and CiviCRM using Ansible. 

The server uses Nginx on an AWS micro instance

The automation installs Drupal 7 and CiviCRM on the server in a secure fashion with SSL certificate from https://letsencrypt.org/. 
CiviCRM and Drupal are installed in different databases as this is considered best practice.

Use this as starting point for your own setups.


To be able to use the AWS via Ansible we are going to use boto library so make sure you have that installed. To install it you just need to run this command.

pip install boto

(I assume you already have pip installed so I am not going to detail how this is done.)
Once boto is installed you need to setup your AWS credentials into the home folder (~/.boto)

[Credentials]
AWS_ACCESS_KEY_ID=...
AWS_SECRET_ACCESS_KEY=…

Update that to match your credentials.
Once that step is completed you can run the installation playbook.

Change directory to the directory holding the ansible yml files.

$ ansible-playbook site.yml

For a more verbose output use -vvv

$ ansible-playbook -vvv site.yml 

Of course you might wanna do own configs within the files.

Like it? -> Enjoy it ! -> Star. 

Thanks.
