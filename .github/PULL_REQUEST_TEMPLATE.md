
<!-- If this PR is not about "apps", we recommend that you use this query parameters instead "?expand=1&template=other_work.md" -->

<!-- Replace title placeholders with proper information -->
<!--
The "PR Title" should follow something like :
Action | PR Title example
-------|-------
Add    | %%manifest%% : Add version %%version%%
Update | %%manifest%% : Update %%field-or-section%%
Remove | %%manifest%% : Remove %%Short_reason%%
   ... | %%manifest%% : %%Short-explanation%%
-->

<!--
  For Work In Progress Pull Requests, please use the Draft PR feature,
  see https://github.blog/2019-02-14-introducing-draft-pull-requests/ for further details.

  For a timely review/response, please avoid force-pushing additional
  commits if your PR already received reviews or comments.

  Before submitting a Pull Request, please ensure you've done the following:
  - 📖 Read the Contributing Guide: https://github.com/brave-simpletons/scoop-the-business/blob/HEAD/.github/CONTRIBUTING.md.
  - 👷‍♀️ One PullRequest per new App manifest.
  - 📝 Use descriptive commit messages.
-->

## What type of Apps related PR is this? (check all applicable)

- [ ] ✨ Add Manifest
- [ ] ♻️ Refactor
- [ ] 🐛 Bug Fix
- [ ] 👷 Optimization
- [ ] 🚩 Other

## Description
<!-- Please do not leave this blank -->

## Related Tickets & Documents
<!-- Please use this format link issue numbers: Fixes #123 https://docs.github.com/en/free-pro-team@latest/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword-->

## Did you verify the followings
<!-- Prepare each script to validate Using: `$manifest = "manifest-name"` -->

### Add/Modify a description in the manifest?
<!-- Using: `.\bin\describe.ps1 $manifest` -->

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Check URLs?
<!-- Using: `.\bin\checkurls.ps1 $manifest` -->

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Update to the latest version?
<!-- Using: `.\bin\checkver.ps1 $manifest -Update` -->

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Update Hashes?
<!-- using: `.\bin\checkhashes.ps1 $manifest -Update` -->

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Format the json manifest?
<!-- Using: `.\bin\formatjson.ps1 $manifest`-->

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

## Did you identify extra steps

### Notes in the manifest?

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Application Dependencies?

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Application Suggestions?

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Pre-installation steps to perform?

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### Post-installation steps to perform?

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

### File persistence to perform?

- [ ] 👍 yes
- [ ] 🙋 yes, but I need help
- [ ] 🙅 no, because they aren't needed

## [optional] What gif/emoji best describes this PR or how it makes you feel?
<!-- You can choose the best that suits you (because YOLO!) : https://www.webfx.com/tools/emoji-cheat-sheet/ -->
<!-- You can use the ones proposed : https://gitmoji.dev/ -->
