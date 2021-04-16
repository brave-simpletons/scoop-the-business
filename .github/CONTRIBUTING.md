# How to Contribute

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
