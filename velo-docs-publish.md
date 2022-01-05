## Setup

 - get permission for repo! ERROR: Permission to wix/wix-code-docs.git denied to michaelho-wix.
 - clone https://github.com/wix-private/velo-docs

## Editing
- find some text near the bug
 - confirm it's the correct file :-)
 - find a standard template
 - adjust template text to fit new context
 - edit buggy file
 - typedef / param (really needs to be a template :-)
 - git checkout branch
 - get on the same level as package.json and velo-docs - this must be the (sub)folder where the module you're working on is stored.
 - npm install
 - git checkout -b michaelho-bug-day-suppressauth
 - make pull request in source
 - make pull request in docs: https://github.com/wix/wix-code-docs/
 - find branch in https://samm140.wixsite.com/reference-branches
 - send for review including PR in source, link to the wix-code-docs PR and the branch preview (put them on the velo-docs PR)

## Run docworks

 - converts jsdoc into json for docs viewer
 - running docworks on e.g. velo-docs creates a branch in the wix-code-docs repo

```
npm run docworks -- --branch MY_BRANCH
```

## Publish doc
- After merging your branch in wix-code-docs, do not run Team City and Lifecycle (won’t work).
 - Open Firebase Fire Console (link fills in relevant fields).
 - Select the viewerId checkbox.
 - Paste the following wix-code-docs ID in the box under viewerId: 2cf3ab73-dbcb-425c-bd3f-682b4f80c135.
 - If you are publishing SPI docs, paste this ID: eeb09edc-c812-43da-a310-9156f5618ecd


 - Click Send.
 - Check your changes in the reference.
 - If there’s an issue, contact the team on the wix-docs-velo Slack channel.

## 

https://bo.wix.com/wix-docs-backstage/projects/563b9c1e-c9c7-4276-a9d4-31c3536a0752/sites/2cf3ab73-dbcb-425c-bd3f-682b4f80c135/branches#active

## old doc

https://docs.google.com/document/d/1B_36l6baqZqZVXujmh8SOHmnrO6HV_wwcrhhVPo7RFc/edit#
