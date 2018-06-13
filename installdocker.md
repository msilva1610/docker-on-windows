#Instalar o docker no windows Server 2016
```
install-module dockerprovider -force
install-package docker -providername dockerprovider -force
```
```
Name                           Version          Source           Summary
----                           -------          ------           -------
Docker                         17.06.2-ee-13    Docker           Docker for Windows Server 2016
```

```
PS C:\Users\vagrant> docker version
Client:
 Version:       17.06.2-ee-13
 API version:   1.30
 Go version:    go1.8.7
 Git commit:    ac44d73
 Built: Mon Jun  4 16:46:59 2018
 OS/Arch:       windows/amd64

Server:
 Engine:
  Version:      17.06.2-ee-13
  API version:  1.30 (minimum version 1.24)
  Go version:   go1.8.7
  Git commit:   ac44d73
  Built:        Mon Jun  4 16:58:47 2018
  OS/Arch:      windows/amd64
  Experimental: false

```
