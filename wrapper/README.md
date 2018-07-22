# What is this?

cp-installssl-wrapper, a bash script to automate Let's Encrypt SSL certificate renewals and installation to with cPanel's JSON API

It depends on [acme.sh](https://github.com/Neilpang/acme.sh) to create/renew the certificates and [cp-installssl](https://github.com/juliogonzalez/cp-installssl) to install them.

Ideally you should call this script from Cron so you don't ever need to take care of the renewals.

# How to use it?

1. Install acme.sh and issue the certificates(s) for the first time.
2. Clone this repository.
3. Follow [instructions](../README.md) to configure cp-installssl.
4. Learn how to run this wrapper with:
   ```
   ./cp-installssl-wrapper -h
   ```
5. Use the wrapper to force a certificate renewall and install it to cPanel.
6. Create a crontab job to call the wrapper and take care of further renewals and installations.

You can get more details about the steps above by following the [step by step tutorial](https://www.juliogonzalez.es/lets-encrypt-ssl-certificates-at-cpanel-without-native-support-for-example-at-namecheap) I created to explain how I configured my Namecheap account.

# License

[WTF Public License](http://www.wtfpl.net/)
