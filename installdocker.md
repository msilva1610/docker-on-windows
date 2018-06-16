# Instalar o docker no windows Server 2016


## Instalar o Windows Container Features
```
install-windowsfeature containers
```

## Reiniciar o Windows
```
Restart-Computer
```

## Instalar o docker

Criar uma pasta para manter os arquivos de execução do Docker. De prefência na pasta padrão do Windows Program and Files

## Download do Dockerd e docker
```
http://aka.ms/tp5/b/dockerrd
http://aka.ms/tp5/b/docker
```

Copiar os arquivos para a pastar de docker criada anteriormente

Criar um System Path para os arquivos serem localizados pelo prompt de comandos

## Registrar o Dockerd no Service

No powershell, digite o comando:
```
docker --register-service
```
start-service docker
```

Faça uma nova verificação
```
get-service docker
```

Verificar a instalação com docker version
```
docker version
```
E, docker info

```
docker info
```

## Instalar os packages providers

```
install-packageprovider containerimage -force
```

# Encontre as images do provider
```
find-containerimage
```

#Instalar o container com powershell
```
install-containerimage windowssercore
```

# Reiniciar o docker
```
restart-service docker
```

```
install-module dockerprovider -force
install-package docker -providername dockerprovider -force
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
