# Project setup

## Dev / PM / TW - create Third Party App (TPA) use case
Instructions
- [ ] [guidelines](https://bo.wix.com/wix-docs/rnd/platformization-guidelines/pm-documentation-checklist)
- [ ] [markdown templates](https://github.com/wix-private/wad-docs-internal-rnd/tree/master/markdown-templates)
- [ ] [Google Docs template (only use as last resort)](https://docs.google.com/document/d/1ZnIQGSTHI3GGrzRj0vYliylqo_bgxoogqfhoqYhuE-k/edit?usp=sharing)

- [ ] use cases (for 3rd party app devs, not only for site owners and/or site users)
- [ ] terminology
- [ ] limitations

## Dev - create internal docs

Instructions:
https://bo.wix.com/wix-docs/rnd/wix-docs/wix-docs/how-to-generate-documentation

## Dev - Create public draft

Instructions:
https://bo.wix.com/wix-docs/rnd/platformization-guidelines/private-share-alpha-version-of-the-docs

- In `documentation.yaml` 

```yaml
apiDoc:
  title: Wix Blah
```
The slug will be `wix-blah`, add it into this URL pattern:

```
https://dev.wix.com/api/rest/drafts/wix-blah?branch=wix-blah
```

**WARNING** Replace the `drafts` part of the routing with `wix-blah` when using this URL in the docs themselves.

## Dev - Generate Auto EDM

Instructions:
https://github.com/wix-private/edm-autogen/blob/master/README.md

## Dev & TW - collect contacts & links:

 - REST Github repo (proto):
 - REST internal docs:
 - REST public draft:
<hr>

 - Velo Auto EDM repo:
 - Velo Docs repo:
<hr>


 - Fire console artefact: https://pbo.wix.com/fire-console/
 - Test site:
<hr>


 - PM:
 - Dev contact:
 - API Master:
 - Slack channel:
 - Monday pulse:
<hr>


 - Third party application use case:
 - Product design doc:
 - Miro diagram: https://miro.com/

# Review - Dev & TW

## REST Doc issues
- [ ] use case(s)
- [ ] third-party access
- [ ] naming
- [ ] object design

## Velo Doc issues
- [ ] naming
- [ ] comparison with REST
- [ ] p13n rules

# Release - TW

## REST Release
 - [ ] last TW read over
 - [ ] final review with REST team lead
 - [ ] set up scopes
  - [ ] Record in [spreadsheat](https://docs.google.com/spreadsheets/d/1FvbXWI4pPVVy2_xSmB8cQRoijcLJvNl3Bbki05xB_RA/edit#gid=0)
  - [ ] Add in [catalog](https://bo.wix.com/wow/permissions/permission-catalog)

 - [ ] check links:

INTERNAL version:
```https://bo.wix.com/wix-docs/rest/drafts/<service-name>/<endpoint>```
EXTERNAL version: 
```https://dev.wix.com/api/rest/<service-name>/<endpoint>```

 - [ ] prep for publish

## Velo Release
 - [ ] last TW read over
 - [ ] final review with Velo team lead
 - [ ] check links
 - [ ] prep for publish

Instructions: https://github.com/michaelho-wix/michaelho-wix/blob/main/velo-docs-publish.md

## Wix Docs Backstage

https://bo.wix.com/wix-docs-backstage/projects

#### Archive

Spreadsheet or other format reviews.
