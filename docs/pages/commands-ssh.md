# SSH

## Check ssh keygen
```
cat ~/.ssh/id_rsa.pub
```

## Generate ssh key
```
ssh-keygen -t rsa -C "email@email.com" -b 4096
```

## Copy ssh key
```
pbcopy < ~/.ssh/id_rsa.pub
```

