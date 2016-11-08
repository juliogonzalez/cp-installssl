# What is this?

cp-installssl, a PHP script to install SSL certificates with cPanel's JSON API

It is heavily based on [code](https://geneticcoder.blogspot.com.es/2014/07/using-cpanels-json-api-with-php-curl-to.html) by [Rob Parham](https://plus.google.com/118182322818308613582).

# Why? 

I created the script specifically to upload [Let's Encrypt SSL](https://letsencrypt.org/) certificates to Namecheap shared hosting, which does not support Let's Encrypt out of the box.

In fact you can request SSH access your Namecheap shared hosting, install [acme.sh](https://github.com/Neilpang/acme.sh), a cron job to renew the certificates and use this script to instal them.

Obviously you can use to automate any other SSL configuration with a certificate from other providers.

# How to use it?

To get help just run:
```
 ./cp-installssh
```
You will need an INI file with the configuration (host, port, user, password...) to access your CPanel. You can either place it at ~/.cp-installssl.ini or create an environment variable CPINSTALSSL_CFG to point to any other file with the config.

You have an example at this very same repository.

# Restrictions

The script will only work with cPanel installations supporting the JSON API v2, and using SSL.

Also note that you will need cURL enabled in PHP at the instance where you plan to run this script (does not need to be the same running cPanel.
