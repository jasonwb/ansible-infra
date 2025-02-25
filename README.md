# ansible-infra
# Ansible Infrastructure Repository Structure

ansible-infra/
│── inventory/         # Inventory files for Ansible
│   ├── hosts.ini      # Define all servers here
│── roles/             # Ansible roles for structured playbooks
│   ├── webserver/     # Nginx setup
│   │   ├── tasks/
│   │   │   ├── main.yml           # Main tasks for installing & configuring Nginx
│   │   ├── handlers/
│   │   │   ├── main.yml           # Restart Nginx if config changes
│   │   ├── templates/
│   │   │   ├── nginx.conf.j2      # Jinja2 template for Nginx config
│   │   ├── files/
│   │   │   ├── index.html         # Default HTML file for testing
│   │   ├── vars/
│   │   │   ├── main.yml           # Variables for the role (optional)
│   │   ├── defaults/
│   │   │   ├── main.yml           # Default values (optional)
│   │   ├── meta/
│   │   │   ├── main.yml           # Role metadata (optional)
│   │   ├── README.md              # Documentation for this role
│   ├── database/      # MySQL setup
│   │   ├── tasks/
│   │   │   ├── main.yml           # Install MySQL and configure database
│   ├── monitoring/    # Logging & monitoring setup
│   │   ├── tasks/
│   │   │   ├── main.yml           # Install Prometheus & Node Exporter
│── playbooks/         # Ansible playbooks
│   ├── setup.yml      # Main playbook
│   ├── web.yml        # Configures web01
│   ├── db.yml         # Configures db01
│   ├── monitoring.yml # Configures monitor01
│── group_vars/        # Variables for each server group
│   ├── all.yml        # Global vars
│── ansible.cfg        # Ansible config file
│── README.md          # Project documentation
