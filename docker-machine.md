# Instalação e uso do Docker Machine

Documentação: https://docs.docker.com/installation/windows/

## Instalação (via Chocolatey)

```
choco install docker-machine --version 0.4.1. -y
```

## Verificando a versão

```
docker-machine -v
```

## Criando uma máquina

```
docker-machine create --driver virtualbox dm1
```

## Listando as máquinas existentes

```
docker-machine ls
```

## Obtendo informações de ambiente para a máquina

No PowerShell:

```
docker-machine.exe env --shell powershell dm1 | Invoke-Expression
```

No Cygwin:
```
eval $(docker-machine.exe env --shell bash dm1)
```

## Executando o hello-world:

```
docker run hello-world
```

## Problemas:

* No PowerShell não mostra corretamente o status da VM, quando é aberta a interface gráfica do VirtualBox
