# obdi-vagrant

A vagranfile for installing and running  [Obdi]( https://github.com/mclarkson/obdi ) in a sandbox environment

Use:

1. Install Virtualbox https://www.virtualbox.org/wiki/Downloads
2. Install Vagrant https://www.vagrantup.com/downloads.html
3. cd \obdi-vagrant
4. run vagrant up

you should see at the end:

```
> default: Starting obdi:
==> default: [  OK  ]
==> default: Starting obdi-worker:
==> default: [  OK  ]
```

5. go to https://localhost:4443/manager/admin on you local machine 
use admin/admin

6. add a user

7. go to https://localhost:4443/manager/run

login using the credentials from step 6

