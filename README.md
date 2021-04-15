# Scoop the Business Bucket

[![GitHub](https://img.shields.io/github/license/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business/blob/main/LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/brave-simpletons/scoop-the-business/main?logo=git&logoColor=white)](https://github.com/brave-simpletons/scoop-the-business/commits/main)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business/pulls)
[![GitHub issues](https://img.shields.io/github/issues/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business/issues)
[![GitHub contributors](https://img.shields.io/github/contributors-anon/brave-simpletons/scoop-the-business)](https://github.com/brave-simpletons/scoop-the-business)

![logo scoop-the-business](images/scoop-the-business.png)

Another bucket for scoop

> :construction:
>
> It is still a `Work in progress`
>
> :construction:

## How to use our bucket

To use it, only add our bucket into scoop:

`scoop bucket add business 'https://github.com/brave-simpletons/scoop-the-business.git'`

## Contributing

To be able to contribute, you will need to create a PullRequest (from a branch or a fork). We suggest one PullRequest per app manifest

Any new app manifest should follow the contribution rules described by Ash258 - since our repo is based on his template and work : [Contributing - How to write manifests](https://github.com/Ash258/Scoop-Ash258/blob/main/.github/CONTRIBUTING.md)

Locally, after creating one manifest, you should execute the ps1 scripts in the bin folder ("manifest.json" is optional - in that case it will run for all manifests):

```powershell
.\bin\checkhashes.ps1 "manifest.json" -Update
.\bin\checkurls.ps1 "manifest.json"
.\bin\checkver.ps1 "manifest.json" -Update
.\bin\describe.ps1 "manifest.json"
.\bin\formatjson.ps1 "manifest.json"
```

## References used to start this project

- Proposed template : [GenericBucket](https://github.com/Ash258/GenericBucket)
- Automation : [Scoop-Ash258](https://github.com/Ash258/Scoop-Ash258)
- [Scoop Wiki Buckets](https://github.com/lukesampson/scoop/wiki/Buckets)
