# Example script of automation on OpenStack

## Conditions

That example will work under following conditions:

Your project will have:

- two networks available: "Ext-Net" and "Private-Net"
- image named "Ubuntu 16.04"
- flavor named "s1-4"

You need to have `openrc.sh` with OpenStack credentials.

## How to use

```
source openrc.sh
ansible-playbook playbook-1.yml
```

## What will happen

That example uses OpenStack to install and configure two instances:

- web-1
- db-1

web-1 will have installed Docker with two containers:

- nginx
- wordpress

Nginx will be used as frontend for Wordpress application.

db-1 will have DB configured which will listen on interface from "Private-Net".
