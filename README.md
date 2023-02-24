# dlb (Dead Letter Box)

`dlb` makes a `GET` request to a provided URL. If the `GET` request returns HTTP `200 OK` the provided command will be executed.

`dlb` functions as a digital "Dead Letter Box" or "Dead Drop" used in the physical world of espionage. Once something appears in the dead letter box (URL), take a corresponding action (execute a command).

One great use case for `dlb` is to remotely trigger automations on your home network without needing to poke pinholes in your home firewall. Cron `dlb` with the URL of a file in your public GitHub repo and once it appears reboot your home PC.

# Installation

```
curl -O https://raw.githubusercontent.com/phuber92/dlb/main/dlb
```

# Usage

```
dlb [url] [command]
```

## Example

```
dlb https://raw.githubusercontent.com/phuber92/lightswitch/main/on cp ~/foo ~/bar
```

# To-Do

1. Rewrite in `rust` and publish binaries for all possible OS/arch combinations.
