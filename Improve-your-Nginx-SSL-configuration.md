# Fix OpenSSL Padding Oracle vulnerability

```
sudo apt-get install --only-upgrade libssl1.0.0 openssl
```

# Improve your Nginx SSL configuration

```
add_header Strict-Transport-Security max-age=63072000;
```

#It actually goes as far as redirecting all HTTP traffic to HTTPS
```
server {
    listen 80;
    server_name <my_server_name>;
    return 301 https://$host$request_uri;
}
```

```
ssl_protocols TLSv1 TLSv1.1 TLSv1.2;  # drop SSLv3 (POODLE vulnerability)
ssl_session_cache shared:SSL:10m;
ssl_session_timeout 10m;
```


```
ssl_prefer_server_ciphers on;
ssl_ciphers 'ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-AES256-GCM-SHA384:DHE-RSA-AES128-GCM-SHA256:DHE-DSS-AES128-GCM-SHA256:kEDH+AESGCM:ECDHE-RSA-AES128-SHA256:ECDHE-ECDSA-AES128-SHA256:ECDHE-RSA-AES128-SHA:ECDHE-ECDSA-AES128-SHA:ECDHE-RSA-AES256-SHA384:ECDHE-ECDSA-AES256-SHA384:ECDHE-RSA-AES256-SHA:ECDHE-ECDSA-AES256-SHA:DHE-RSA-AES128-SHA256:DHE-RSA-AES128-SHA:DHE-DSS-AES128-SHA256:DHE-RSA-AES256-SHA256:DHE-DSS-AES256-SHA:DHE-RSA-AES256-SHA:!aNULL:!eNULL:!EXPORT:!DES:!RC4:!3DES:!MD5:!PSK';
```

# Generate your DH parameters with OpenSSL:
```
cd /etc/ssl/certs
openssl dhparam -out dhparam.pem 4096
```

Nginx configuration:
```
ssl_dhparam /etc/ssl/certs/dhparam.pem;
```

# OCSP stapling
```
add_header X-Frame-Options DENY;
```
