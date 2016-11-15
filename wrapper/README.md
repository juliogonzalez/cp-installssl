# What is this?

cp-installssl-wrapper, a bash script to automate Let's Encrypt SSL certificate renewals and installation to with cPanel's JSON API

It depends on [acme.sh](https://github.com/Neilpang/acme.sh) to create/renew the certificates and [cp-installssl](https://github.com/juliogonzalez/cp-installssl) to install them.

Ideally you should call this script from Cron so you don't ever need to take care of the renewals.

# How to use it?

To get help just run:
```
 ./cp-installssl-wrapper -h
```

# License

[WTF Public License](http://www.wtfpl.net/)
