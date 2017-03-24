# obdi-vagrant

A vagrantfile for installing and running  [Obdi]( https://github.com/mclarkson/obdi ) in a sandbox environment

Use:

Install the following:
1.  Install Virtualbox https://www.virtualbox.org/wiki/Downloads
2.  Install Vagrant https://www.vagrantup.com/downloads.html

3. Run these commands:
```javasctipt
git clone https://github.com/Hbouaz/obdi-vagrant.git
cd obdi-vagrant
vagrant up --provider virtualbox
```

you should see at the end:

```shell
> default: Starting obdi:
==> default: [  OK  ]
==> default: Starting obdi-worker:
==> default: [  OK  ]
```

4. Go to https://localhost:4443/manager/admin on you local machine 

Login...

```shell
user/password admin/admin
```

5. Add a user

6. go to https://localhost:4443/manager/run

login using the credentials from step 5

