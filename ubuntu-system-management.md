# ubuntu system management

Sync system time with NTP
```sh
sudo ntpdate -s ntp.ubuntu.com
```

List all timezones
```sh
timedatectl list-timezones
```

Update timezone to Hong Kong
```sh
sudo timedatectl set-timezone Asia/Hong_Kong
```


