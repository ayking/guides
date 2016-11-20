# Let's Encrypt for (AWS + nginx + Ubuntu 14.04) - Free SSL/TLS Certificates

Install certbot-auto
```sh
wget https://dl.eff.org/certbot-auto
chmod a+x certbot-auto
```

Update nginx default config (redirect all http request to https except the path /.well-known/acme-challenge since Let's Encrypt will access this path when create/update certifications)

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

```
sudo service nginx reload
```

Setup certbot-auto 

```sh

mkdir /tmp/letsencrypt-auto

# This sample is SAN (subject alternativ name) for example.com and www.example.com
./path/to/certbot-auto certonly --webroot -w /tmp/letsencrypt-auto -d example.com -d www.example.com

# reload nginx
sudo service nginx reload

```

You can find the SSL certification path on the `console output`. 

Update nginx ssl certification settings (nginx use `fullchain.pem` and `privkey.pem`)
```
server {
	ssl on;
	ssl_certificate path\to\ssl\certification;
	ssl_certificate_key path\to\ssl\key;
	ssl_protocols TLSv1.2;
}
```

Last but not the least, certification create/renew only valid for 90 days so you need to add a cron job to update it regularly 

Create renewal script (www_renew.sh)
```
/path/to/certbot-auto renew
sudo service nginx reload
```

```sh
0 7,19 * * * sh /path/to/www_renew.sh >> path/to/log
```

If we ran the staging config before then we need to do delete the following folder 
```
/etc/letsencrypt/accounts/acme-staging.api.letsencrypt.org
```

## Ref
- https://letsencrypt.org/getting-started/
- https://letsencrypt.org/docs/rate-limits/
- https://certbot.eff.org/#ubuntutrusty-nginx
