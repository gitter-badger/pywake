This is a simple python script I wrote to manage my wake-on-lan needs. It expects a config file named .wakefile.json in your home directory. This makes it possible to include the python script and the config file in your dotfiles repo if you happen to have them under version control. This script uses the [awake library](https://pypi.python.org/pypi/awake) to send the magic packet.

This code was tested on linux only. It doesn't work on windows due to the way the pinging works. I think it should work on Mac OS X, but this is untested. If you happen to find any gotcha's, feel free to create a pull request. 

The config file should look like this:
```json
{
    "hostname" : {
        "mac" : "xx:xx:xx:xx:xx:xx",
        "ip" : "10.0.0.101"
    },
    "hostname" : {
        "mac" : "xx:xx:xx:xx:xx:xx",
        "ip" : "10.0.0.102"
    }   
}
```

The animate() function is from [StackOverflow](http://stackoverflow.com/a/22029635/3270483).

The pingUntilUp() function is based on [this](http://stackoverflow.com/a/12490356) StackOverflow answer.

The rest of this code is available under the MIT license. 
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/martijnvandijk/pywake?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)