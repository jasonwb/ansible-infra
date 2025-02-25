1. Update the file with your actual IPs & username.
2. Test the connection from Ansible Master:


ansible -i inventory/hosts.ini all -m ping

Clone the repository

git clone https://github.com/jasonwb/ansible-infra.git
cd ansible-infra

Modify inventory & playbooks as needed

   1.  Add your server IPs to hosts.ini.
   2.  Adjust setup.yml to match your automation needs.

Run Ansible Playbook

ansible-playbook -i inventory/hosts.ini playbooks/setup.yml
