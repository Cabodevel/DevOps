
# 1 Ping to check inventory

    ansible -i inventory all -u demobook -m ping
    
    The -i argument is the path of the inventory file
    the -u argument corresponds to the remote username that's used to connect to the remote machine
    -m is the command to execute.

# 2 Run a playbook

    ansible-playbook -i inventory playbook.yml
    
    The -i argument with the inventory file **path**

    Run a playbook asking for vault pass to decrypt sensitive info
    ansible-playbook -i inventory playbook.yml --ask-vault-pass

# 3 Dry run

    ansible-playbook -i inventory playbook.yml --check

# 4 Encrypt sensitive info

    ansible-vault encrypt group_vars/database/main.yml

# 5 Decrypt sensitive info

    ansible-vault decrypt group_vars/database/main.yml
