# Monitoring Docker swarm from Zabbix

fork from https://github.com/kulpin74/zabbix-swarm

Replacing the docker html api with running UserParameters on the agent, performing curl --silent --unix-socket /var/run/docker.sock http://v1.41/... on the socket itself.
To make this work, the user running the zabbix agent (usually called zabbix) needs access to the docker socket. 

sudo usermod -aG docker zabbix
