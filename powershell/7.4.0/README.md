# Powershell v7.4.2 with WSMan
Dockerfile uses alpine:3.17 to build a Linux based Powershell container with WSMan embedded in it
You can use this container via Gitlab (linux based)Runners using the following code
```
stages:
    - deploy

pwsh:
    stage: deploy
    image: mylocalrepo.contoso.com/project1/powershell:7.4.2
    script:
      -  hostname  
      -  pwsh -command get-childitem
```
## Dockerfile source
[Source](https://github.com/PowerShell/PowerShell-Docker/blob/master/release/7-4/alpine317/docker/Dockerfile)

## Releases
[Release](https://github.com/PowerShell/PowerShell/releases/tag/v7.4.2)

## WSMan
```
# enable WSMan
  Install-Module -Name PSWSMan -f ; \
  Start-Sleep -Seconds 15 ; \
  Install-WSman ; \
  Start-Sleep -Seconds 5 ; \
```
