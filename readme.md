##  ANSIBLE-VAULT ENCRYPT WAS USED FOR GROUP_VARS FOR SECURITY PURPOSES.

**To dencrypt**

`ansible-vault decrypt group_vars/all.yml`

Pass: Faith2020@

**To run ansible-playbook with the hng Server**

### 1. Run the server-setup first with the server-keypair to copy the sshkey and install nginx, postgres, composer and PHP

`ansible-playbook server-setup.yml -i hosts -u ubuntu --key-file ansible-keypair.pem`

### 2. Then run the laravel-deploy to install laravel and the necessary periquisites

`ansible-playbook laravel-deploy.yml -i hosts -u ubuntu`

