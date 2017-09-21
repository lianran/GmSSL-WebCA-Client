# get-sm2-cert

This project is forked from [srvrco/getssl](https://github.com/srvrco/getssl) and depends on the [GmSSL](http://gmssl.org).


This doc just a simple guide to obtain SSL SM2 cert and you can learn how to use getssl from [srvrco/getssl](https://github.com/srvrco/getssl) or the [old_README.md](./old_README.md).


## Installation

You'll find the latest version in the git repository:

```
git clone https://github.com/lianran/GmSSL-WebCA-Client.git
```

In addition you must install the GmSSL and you can find the guide from [here](http://gmssl.org).


## How to obtain a SM2 certificates

Once you have obtained the script and installed the GmSSL(see Installation above), the next step is to use


```./getssl -c yourdomain.com```

where yourdomain.com is the primary domain name that you want to create a certificate for.   This will create the following folders and files.

```
~/.getssl
~/.getssl/getssl.cfg
~/.getssl/yourdomain.com
~/.getssl/yourdomain.com/getssl.cfg
```

You can then edit ~/.getssl/getssl.cfg to set the values you want as the default for the majority of your certificates.

Then edit ~/.getssl/yourdomain.com/getssl.cfg to have the values you want for this specific domain (make sure to uncomment and specify correct `ACL` option, since it is required).

You can then just run;

```getssl yourdomain.com ```

and you will obation SM2 cert if there is no error.