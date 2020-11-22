# ansible
pip3 install ansible
#all nodes must have python installed
ansible --version
echo "[webservers]" >inventory
echo "10.xx.xx.xx" >>inventory
ansible -i inventory webservers -m ping -u root
echo "[defaults]" > ansible.cfg
echo "INVENTORY = inventory" >>ansible.cfg
ansible webservers -a"free -h" -u root
ansible init ubuntu
create playbook
ansible provision
