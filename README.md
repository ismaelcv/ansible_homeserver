# ansible-homeserver
The Ansible code for my [Ansible Home Server series](https://www.youtube.com/playlist?list=PLkxWXio1KmRoZd88WbrnSnQM5MJY5PjH2)

Commits represent individual video parts:
* [Part 1 – Installation, Environment, Inventory, Tasks & Variables](https://github.com/notthebee/ansible_homeserver/tree/2eef7ab66f4f97b1107a12e5f0c84455efb477fc)
* [Part 2 – Roles, Handlers, Ansible Galaxy, Filters & Loops](https://github.com/notthebee/ansible_homeserver/tree/1a67056b0d0825bc00fa7c800d47ff04298df6df)



# Set up ssh
ssh-keygen -o -a 100 -t ed25519 -f ~/.ssh/homeserver -C ismaelcv@gmail.com
ssh-copy-id -i ~/.ssh/homeserver ismael@192.168.1.77 

Set up vault
ansible-vault create secret.yml
ansible-vault edit secret.yml
password:esteesmipass
:wq

# Run ansible
ansible-playbook --ask-vault-pass run.yml


# Login to server via ssh
ssh ismael@192.168.1.77  


 ansible all -m ping 