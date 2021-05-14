# How to Contribute

To be able to contribute, you will need to create a PullRequest (from a branch or a fork). We suggest one PullRequest per app manifest

Any new app manifest should follow the contribution rules described by Ash258 - since our repo is based on his template and work : [Contributing - How to write manifests](https://github.com/Ash258/Scoop-Ash258/blob/main/.github/CONTRIBUTING.md)

## Working on manifests

Each manifest should be in separated branch

### Creating new manifest

To help create new manifest, you can use the "snippets" available in `.vscode\json.code-snippets`.

### Before pushing the new manifest

Locally, after working on a manifest, you should execute the ps1 scripts in the bin folder ("manifest.json" is optional but highly recommended - if omitted it will run all manifests checks and it will take nearly forever :wink:):

```powershell
# replace the %%MANIFEST-NAME%% with the right name
$manifest = "%%MANIFEST-NAME%%"

.\bin\describe.ps1 $manifest
.\bin\checkurls.ps1 $manifest
.\bin\checkver.ps1 $manifest -Update
.\bin\checkhashes.ps1 $manifest -Update
.\bin\formatjson.ps1 $manifest
```

## Pull Request

For app manifests, there is a template that we recommend to use. It will guide to some validations before submitting.

Also we recommend that you add the team "brave-simpletons/bashful" as reviewers.

### Actions & Bot

On a pull request creation, an Action will run that will validate some part of the content. At the end a little report will be shown.

- If it passed, you will need to wait for a reviewer's approval before completing the PR
- If failed you should see missing checkmarks that will tell you on what you should work on. When you think you has resolve the issue (or needed any other changes), you must post the comment "/verify" in the PR and it will relaunch the Action.
