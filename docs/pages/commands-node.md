# Node

## NVM

## Install specific version of node
```
nvm install v8.9.4
```

## Set default node version
```
nvm alias default v8.9.4
```

## Use a specific node version for a project
From the directory where the project is located
```
nvm use v9.5.0
```

## Uninstall Node.js

Check any updates [here](https://gist.github.com/TonyMtz/d75101d9bdf764c890ef)

First:
```
lsbom -f -l -s -pf /var/db/receipts/org.nodejs.pkg.bom | while read f; do  sudo rm /usr/local/${f}; done
sudo rm -rf /usr/local/lib/node /usr/local/lib/node_modules /var/db/receipts/org.nodejs.*
```

To recap, the best way (I've found) to completely uninstall node + npm is to do the following:

Go to `/usr/local/lib` and delete any `node` and `node_modules`
```
cd /usr/local/lib
sudo rm -rf node*
```

Go to `/usr/local/include` and delete any `node` and `node_modules` directory
```
cd /usr/local/include
sudo rm -rf node*
```

If you installed with `brew install node`, then run `brew uninstall` node in your terminal
```
brew uninstall node
```

Check your Home directory for any `local` or `lib` or `include` folders, and delete any `node` or `node_modules` from there
Go to /usr/local/bin and delete any node executable
```
cd /usr/local/bin
sudo rm -rf /usr/local/bin/npm
sudo rm -rf /usr/local/bin/node
ls -las
```

You may need to do the additional instructions as well:
```
sudo rm -rf /usr/local/share/man/man1/node.1
sudo rm -rf /usr/local/lib/dtrace/node.d
sudo rm -rf ~/.npm
```