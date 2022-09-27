
### Install

```console
sha256sum ~/Downloads/Anaconda3-2021.11-Linux-x86_64.sh
```
```console
bash ~/Downloads/Anaconda3-2021.11-Linux-x86_64.sh
```

### Set the auto_activate_base on

```console
conda config --set auto_activate_base true
```

### Set the auto_activate_base off
```console
conda config --set auto_activate_base false
```


### Create new enviroment

```console
conda create -n newEnvName python=3.6
```

### List all enviroment

```console
conda info --env
```

### Rename enviroment

```console
conda rename -n old_name -d new_name 
```
