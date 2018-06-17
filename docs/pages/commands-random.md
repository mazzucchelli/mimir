# Finder

#### Create symbolic link
```
ln -s /any/place/on/the/disk existing/file/to/link
```

#### Show hidden file on a MAC
```
defaults write com.apple.Finder AppleShowAllFiles true
killall Finder
```

#### Hide hidden file on a MAC
```
defaults write com.apple.Finder AppleShowAllFiles false
killall Finder
```

# Python

## HTTP server
``` python
python -m SimpleHTTPServer 8080
```