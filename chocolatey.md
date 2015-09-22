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

### Oracle JDK 8

* Instalação:
```
choco install jdk8 -y
```
* Atualização:
```
choco upgrade jdk8 -y
```

### Oracle JRE 8

* Necessário para a execução de applets (ex.: site do BB)
* Página para teste: https://www.java.com/en/download/installed.jsp
* Instalação da [versão v8.0.60](https://chocolatey.org/packages/jre8/8.0.60.20150902) (ainda não aprovada no repositório do Chocolatey no momento da escrita deste tópico)
```
choco install jre8 -y --version 8.0.60.20150902
```

### VirtualBox e VirtualBox.ExtensionPack

```
choco install virtualbox VirtualBox.ExtensionPack -y
```

Talvez a versão mais atual do VirtualBox.ExtensionPack possa estar em estado de "waiting". Nessa situação, para baixá-la é possível executar o seguinte comando (exemplo):
```
choco install VirtualBox.ExtensionPack --version 5.0.4.102546 -y
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

## Listagem de pacotes instalados

```
choco list -lo
```
