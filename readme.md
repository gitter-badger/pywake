This is a simple python script I wrote to manage my wake-on-lan needs. It expects a config file named .wakefile.json in your home directory. This makes it possible to include the python script and the config file in your dotfiles repo if you happen to have them under version control. This script uses the [awake library](https://pypi.python.org/pypi/awake) to send the magic packet.

The config file should look like this:
```json
{
    "hostname" : {
        "mac" : "xx:xx:xx:xx:xx:xx",
        "ip" : "10.0.0.101"
    },
    "blackhole" : {
        "mac" : "xx:xx:xx:xx:xx:xx",
        "ip" : "10.0.0.102"
    }   
}
```