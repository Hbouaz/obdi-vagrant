# obdi-vagrant

A vagranfile for installing and running  [Obdi]( https://github.com/mclarkson/obdi ) in a sandbox environment

Use:

Install the following:
1.  Install Virtualbox https://www.virtualbox.org/wiki/Downloads
2.  Install Vagrant https://www.vagrantup.com/downloads.html

Run these commands:
```shell
2.1 git clone https://github.com/Hbouaz/obdi-vagrant.git
3.  cd obdi-vagrant
4.  vagrant up --provider virtualbox
```

you should see at the end:

```shell
> default: Starting obdi:
==> default: [  OK  ]
==> default: Starting obdi-worker:
==> default: [  OK  ]
```

5. Go to https://localhost:4443/manager/admin on you local machine 

Login...

```shell
user/password admin/admin
```

6. Add a user

7. go to https://localhost:4443/manager/run

login using the credentials from step 6

