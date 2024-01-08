# Scoop the Business Bucket

[![GitHub](https://img.shields.io/github/license/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business/blob/main/LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/brave-simpletons/scoop-the-business/main?logo=git&logoColor=white)](https://github.com/brave-simpletons/scoop-the-business/commits/main)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business/pulls)
[![GitHub issues](https://img.shields.io/github/issues/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business/issues)
[![GitHub contributors](https://img.shields.io/github/contributors-anon/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business)

![logo scoop-the-business](images/scoop-the-business.png)

Another bucket for [scoop](https://github.com/lukesampson/scoop)

> :construction:
>
> It is still a `Work in progress`
>
> :construction:

## What is Scoop

Scoop is a command-line installer for windows and will let you install the tools you know and love

### What is a "Bucket" for Scoop

A "bucket" is simply a repository of applications that are shared to be known and installed using the Scoop cli

### Does the applications are updated periodically

YES... We use an GitHub actions that execute many times a day to finds all the newest application versions available and updates the bucket.

## Installing Scoop and use our "Bucket"

> :memo:
>
> Make sure PowerShell 5 (or later, include PowerShell Core) and .NET Framework 4.5 (or later) are installed
>
> :memo:

It's really easy to install and configure Scoop to use our bucket. Just follow the code (or save it in a .ps1 file & execute it):

```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
Invoke-Expression (New-Object System.Net.WebClient).DownloadString("https://get.scoop.sh")

scoop install git

$fileGitConfig = "$env:userprofile\.gitconfig"
if (-not(Test-Path -Path $fileGitConfig -PathType Leaf)) {
    Invoke-WebRequest "https://raw.githubusercontent.com/brave-simpletons/tooling-for-developers/main/git/gitconfig.txt" -OutFile $fileGitConfig
}

scoop bucket add business "https://github.com/brave-simpletons/scoop-the-business.git"
```

## Using scoop

### Getting help

The help is already included in the CLI

```powershell
scoop help
```

For more information, you can also read this [Scoop Guide](https://scoop.netlify.app/)

### Searching an app

Sure, you could search our GitHub repo... But it could be more easier and faster to use the CLI :wink:

```powershell
# scoop search app-name app-name2 [...]
scoop search 7zip vscode
```

### Installing/Uninstall an application

When you know what app to install:

```powershell
# scoop install app-name app-name2 [...]
scoop install 7zip vscode
```

When you know what app to uninstall:

```powershell
# scoop uninstall app-name app-name2 [...]
scoop uninstall 7zip vscode
```

### Updating

Updating scoop itself and the buckets

```powershell
scoop update
```

Afterward, it will be possible to know if updates exists for one of the application installed using:

```powershell
scoop status
```
Then you will be able to decide if you update all applications or only specific ones using one of the following:

- Update all applications

   ```powershell
   scoop update *
   ```

- Updating specific application(s)

   ```powershell
   #scoop update app-name app-name2 [...]
   scoop update 7zip vscode
   ```

### Cleaning the old app versions

Since the app can be installed separately, sometimes you could have a lot of version. It could be a good idea to done some cleanup using:

- Cleaning all applications

   ```powershell
   scoop cleanup *
   ```
   
- Cleaning specific application(s)

   ```powershell
   #scoop cleanup app-name app-name2 [...]
   scoop cleanup 7zip vscode
   ```

Also you could clean the cache of the downloaded application for a specific app or for all

- Removing all applications from the cache

   ```powershell
   scoop cache rm *
   ```

- Removing specific application from the cache

   ```powershell
   #scoop cache rm app-name
   scoop cache rm 7zip
   ```

## What Apps that 'scoop-the-business' suggests

All the app that we use are listed in the folder [bucket](./bucket). If one is missing do not hesitate to contribute or ask us and... we will do it when we will find the time :smile:

## Contributing

You think something is missing here ? Follow [How to Contribute](.github/CONTRIBUTING.md) page and submit your PR :wink:

## References used for this project

- Proposed template : [GenericBucket](https://github.com/Ash258/GenericBucket)
- Automation : [Scoop-Ash258](https://github.com/Ash258/Scoop-Ash258)
- [Scoop Wiki Buckets](https://github.com/lukesampson/scoop/wiki/Buckets)
