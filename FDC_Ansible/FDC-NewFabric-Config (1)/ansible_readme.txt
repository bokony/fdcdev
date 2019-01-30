Ansible Readme:
---------------

1. Install ansible version 2.5 from https://www.ansible.com/

verify the version using the following command.

# ansible --version
ansible 2.5.2
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/root/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.12 (default, Dec  4 2017, 14:50:18) [GCC 5.4.0 20160609]

2. install the following FDC supported Ansible roles from https://galaxy.ansible.com/list#/roles

   - dell-networking.dellos-snmp (v3.0.0)
   - dell-networking.dellos-interface (v3.0.0)
   - dell-networking.dellos-vlan (v3.0.0)
   - dell-networking.dellos-lag (v3.0.0)
   - dell-networking.dellos-vlt (v3.0.0)
   - dell-networking.dellos-lldp (v3.0.0)
   - dell-networking.dellos-system (v3.0.0)
   - dell-networking.dellos-users (v3.0.0)
   - dell-networking.dellos-bgp (v3.0.0)
   - dell-networking.dellos-route-map (v3.0.0)
   - dell-networking.dellos-ecmp  (v3.0.0)
   - dell-networking.dellos-prefix-list (v3.0.1)
   - dell-networking.dellos-xstp (v3.0.0)
   - dell-networking.dellos-dcb (v3.0.0)

    Command to install role:
    $ ansible-galaxy install <Role-Name>

3. Create a fabric and complete the "Network Configuration". Provide the Management IP address of each switch and CLI credentials.

4. Download the Ansible zip file from FDC which is available in "Configuration Download" and extract on the server where ansible got installed. The Zip file contains following files

    - ansible_readme.txt
    - ansible_deploy.sh
    - hosts
    - playbook.yml
    - host_vars folder and its contents (the yml files for each switch in the fabric)
    - templates folder and its contents (the cli command files for each switch in the fabric if required)

5. Provide executable permission for the file ansible_deploy.sh and execute it. Check for the execution status on the console

6. Please make sure that the host key is saved in the ansible server. For more information http://docs.ansible.com/ansible/latest/user_guide/intro_getting_started.html#host-key-checking