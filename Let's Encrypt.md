# Let's Encrypt for (AWS + nginx) - Free SSL/TLS Certificates

Update node version 4.5.0
```sh
curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
```

Install letsencrypt
```sh
npm install -g letsencrypt-cli@2.x
```

Update nginx default config (redirect all http request to https but except the /.well-known/acme-challenge since Let's Encrypt will access this path when create/update certifications)

```sh
sudo vim /etc/nginx/sites-available/default
```

```
server {

  listen  80;
  listen  [::]:80;

  server_name .domain.com;

  location '/.well-known/acme-challenge' {
    default_type  "text/plain";
    root          /tmp/letsencrypt-auto;
  }

  location / {
    return 301 https://$host$request_uri;
  }

}
```

Create script (ssl_www.sh) for create/update staging SSL certificates 
```sh
mkdir /tmp/letsencrypt-auto
letsencrypt certonly \
  --agree-tos --email admin@domain.com \
  --webroot --webroot-path /tmp/letsencrypt-auto \
  --domains www.domain.com,domain.com \
  --server https://acme-staging.api.letsencrypt.org/directory 
sudo service nginx reload
```

Run the script you can find the SSL certification path on the `console output`. 

Update nginx ssl certification settings (nginx use `fullchain.pem` and `privkey.pem`)
```
server {
	ssl on;
	ssl_certificate path\to\sslcertification;
	ssl_certificate_key path\to\ssl\key;
	ssl_protocols TLSv1.2;
}
```

Highly recommend testing against staging environment before using production environment. This will allow you to get things right before issuing trusted certificates and reduce the chance of your running up against `rate limits`.

Move to production environment need to remove `all fake certifications and keys` in the certification folder and update the server to `--server https://acme-v01.api.letsencrypt.org/directory` or remove `--server https://acme-staging.api.letsencrypt.org/directory`

Last but not the least, certification create/renew only valid for 90 days so you need to add a cron job to update it regularly 

```sh
0 7,19 * * * sh /path/to/ssl_www.sh
```


Ref
[https://letsencrypt.org/getting-started/]
[https://github.com/Daplie/letsencrypt-cli/blob/master/README.md]
[https://letsencrypt.org/docs/rate-limits/]
