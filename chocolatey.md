# Instalação e uso do Chocolatey

## Motivação

Finalmente, um gerenciador de pacotes nativo para o Windows: [Chocolatey](http://chocolatey.org). É algo que realmente torna menos chata a utilização do Windows! ;)

## Instalação

### Pelo prompt de comando (como administrador)

```
@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```

### Pelo powershell

```
iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))
```

## Instalação de pacotes

### VirtualBox e VirtualBox.ExtensionPack

```
choco install virtualbox VirtualBox.ExtensionPack -y
```

### Vagrant

```
choco install vagrant -y
```

### Docker e Docker Machine

Instalação do Docker na versão default:

```
choco install docker -y
```

Instalação do [docker-machine](https://chocolatey.org/packages/docker-machine) na versão 0.4.1 (versão no estado de "waiting"):

```
choco install docker-machine --version 0.4.1 -y
```
