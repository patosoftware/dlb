# sowol

Secure Outbound Wake on LAN

# What is `sowol`?

`sowol` will make a `GET` request to a provided URL. If the `GET` request returns a `200` status code a Wake-on-LAN (WoL) magic packet will be sent to the provided MAC address.

When set up correctly you can securely wake a device over the internet without any inbound firewall rules.

One use case I've found useful is to cron `sowol` on a device like a Raspberry Pi on your network. Set the URL to a raw file from a GitHub repo. If the file exists in the repo `sowol` will wake the device and if not it will do nothing. You can then make commits to add and remove the "lightswitch" file from the repo to trigger `sowol` to wake the device or not. This setup works great for waking you gaming PC remotely so you can use Steam Remote Play without having to leave your PC awake 24x7.

# Installation

## Dependencies

Currently `sowol` depends on the `wakeonlan` APT package.

```
sudo apt-get update && sudo apt-get install -y wakeonlan
```

## Download `sowol`

```
curl -O https://raw.githubusercontent.com/phuber92/sowol/main/sowol
```

# Usage

```
sowol [url] [mac_address]
```

# To-Do

1. Rewrite in `rust` and publish binaries for all possible OS/arch combinations.
