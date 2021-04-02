# create user 
https://serversforhackers.com/c/create-user-in-ansible
---
 - name: Create a login user
     user:
      name: fideloper
      password: '???'
      groups: # Empty by default, here we give it some groups
       - docker
       - sudo
      state: present
      shell: /bin/bash       # Defaults to /bin/bash
      system: no             # Defaults to no
      createhome: yes        # Defaults to yes
      home: /home/fideloper  # Defaults to /home/<username>
## setup requirements
sudo dpkg --add-architecture i386; sudo apt update; sudo apt install unzip jq netcat lib32gcc1 lib32stdc++6 steamcmd

## use use csgoserver

## setupd LGSM
https://linuxgsm.com/lgsm/csgoserver/

wget -O linuxgsm.sh https://linuxgsm.sh && chmod +x linuxgsm.sh && bash linuxgsm.sh csgoserver
./csgoserver install auto-install

## new instance https://docs.linuxgsm.com/features/multiple-game-servers
cp csgoserver anotherserver

## config LGSM

## usefull
https://docs.ansible.com/ansible/2.5/user_guide/playbooks_variables.html#passing-variables-on-the-command-line