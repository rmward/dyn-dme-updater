drafts-text-tools
=================

A Mac OS X launch agent to regularly update a dynamic DNS entry for DNSMadeEasy with a machine's current public IP address.

## Usage

This agent comes with a small install.sh script that you can use to install this on Mac OS-X.

Run it as follows:

```bash
./install <username> <password> <record-id>
```

For example,

```bash
./install john123 secretpassword 3241256
```

The script does a couple of things:
* Installs the agent plist file into ~/Library/LaunchAgents directory
* Writes the credentials passed as arguments into the plist file
* Tries to run the DNS update command, to make sure everything works and credentials are valid.
* If DnsMadeEasy returns OK, the agent is automatically started to launchctl.

## Authors

* https://github.com/rmward - agent and project maintainer
* https://github.com/kigster - added install script

## License

MIT

