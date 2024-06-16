# How to update the Go version

For Linux based versions.

### 1. Uninstall the existing version

As mentioned [here](https://golang.org/doc/install#install), to update a go version you will first need to uninstall the original version.

To uninstall, delete the `/usr/local/go` directory by:

```
$ whereis go [eg: go: /usr/bin/go, /usr/local/go]
$ sudo rm -rf /usr/local/go
```

### 2. Install the new version

Go to the [downloads](https://golang.org/dl/) page and download the binary release suitable for your system using `wget`.

```
$ wget https://golang.org/dl/go1.22.4.linux-amd64.tar.gz -O /home/user/go1.22.4.linux-amd64.tar.gz
```

### 3. Extract the archive file

To extract the archive file:

```
$ sudo tar -C /usr/local -xzf /home/user/go1.22.4.linux-amd64.tar.gz
```

### 4. Set up the environment

Add the Go binary to your PATH by adding the following lines to your ~/.profile or ~/.bashrc

```
export PATH=$PATH:/usr/local/go/bin
$ echo $PATH | grep "/usr/local/go/bin"
```

### 5. Reload your profile

Make sure to reload the ~/.profile or ~/.bashrc files

```
source ~/.profile
or
source ~/.bashrc
```

# Go Lang Setup (the easiest way)

### 1. Clone [update-golang](https://github.com/udhos/update-golang) by @udhos Great work man! 
``` 
git clone https://github.com/udhos/update-golang  
cd update-golang  
sudo ./update-golang.sh  
source /etc/profile.d/golang_path.sh
```

### 2. Remove

You can use the 'remove' option to undo update-golang.sh work

```
$ sudo ./update-golang.sh remove
```
