# DevOps Project with Ansible
Developer > Git-Hub > Jenkins > Ansible > Web-Server


# Build
send command or execute command over ssh
rsync -avh /var/lib/jenkins/workspace/Ansible-Project/*    root@172.31.31.209:/opt/

# Post-Build Action
send build artifact over ssh
ansible-playbook   /sourcecode/playbook.yml

# Playbook
- hosts: all
  tasks:
    - copy:
        src: /opt/
        dest: /var/www/html
