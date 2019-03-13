# Thanks For your Help.

## A)FTP Server:
ftp> dir
-rwxr-xr-x    1 1002     1001     110633697 Mar 07 03:56 backendapi-test-SNAPSHOT.jar
-rwxr-xr-x    1 1002     1001           32 Mar 11 03:52 backendapi-test-SNAPSHOT.jar.txt
-rwxr-xr-x    1 1002     1001        16455 Mar 11 08:47 backendapi-test-SNAPSHOT.properties
-rwxr-xr-x    1 1002     1001         3744 Mar 11 05:58 backendapi-test-SNAPSHOT.sh
ftp> pwd
257 "/test/gfh-weixin/api"

## B)Ansible hosts
cat hosts
[app04]
172.16.168.69 ansible_ssh_user=gfhadmin ansible_ssh_pass="xxx"

## C)Extra-vars
Backup Name : date=xxxx
Deploy APP  : app=backendapi-test-SNAPSHOT or app=walletservicesapi-test-SNAPSHOT ...


### example:
ansible-playbook -i hosts gfh_deploy_tool.yaml --extra-vars "backup=20190312  app=backendapi-test-SNAPSHOT  jarport=9000  env=test/gfh-weixin project=api"
ansible-playbook -i hosts gfh_deploy_tool.yaml --extra-vars "backup=20190312  app=ali-api-test  jarport=9070  env=test/gfh-ali project=api"



