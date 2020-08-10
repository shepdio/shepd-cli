# shepd-cli

Standalone CLI for managing resources in your SHEPD account.

SHEPD is a cloud-based service that filters your DNS traffic according to your rules, protecting your applications and cloud infrastructure from outbound traffic to malicious sites, get forewarning of instances behaving suspiciously and, through SHEPD caching, gain performnace.

Requires a free account at https://shepd.io/ to get started.

## Installation

1. Download the [latest release](https://github.com/shepdio/shepd-cli/releases/tag/v0.1.2)

2. Install on your system with dpkg -i shepd-cli_<version>.deb

3. Configure your API keys in `~/.config/shepd/shepd.conf` (hint: the [API keys section of the SHEPD Console](https://shepd.io/console-ng/account) can generate this file for you when you create a new key)

4. Run the CLI with `shepd-cli`

Most resources in SHEPD are supported, with the exception of logging data. Use `shepd-cli help` to get help. This can be used on subcommands too (e.g. `shepd-cli devices help`).

## Getting started

Once installed, you probably want to create a new device. The way to do that is:

```
shepd-cli devices create --name="my device" --token-file="my-device.conf"
```

Once that's done, you'll have a new `my-device.conf` file. You should copy this to `/etc/shepd/shepd.conf` on the system you're using [SHEPD DNS](https://github.com/shepdio/shepd-dns) on to monitor/filter traffic. Create a new 'device' in this way for each system you want to monitor.

## Sources

You'll notice there's no source code in this repository yet. That will change - once the code has undergone proper review and sanity checking, it will be uploaded here.
