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

Detailed instructions: https://docs.google.com/document/d/1D4iYGXU9zvu1M7HsfdI4ZnezTYy0uDCa6yXUMazuPf4/edit

## Dev & TW - collect contacts, info & links:

 - desired location in docs menu tree (table of contents):

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
- [ ] deprecated / hidden fields:
  - to hide a field in the public docs, but keep visisble internally, mark as ____

|Tag|Value|Meaning|Effect(s)|
|---|---|---|---|
|option (wix.api.maturity) |ALPHA|Internal use, in development|?|
|option (wix.api.maturity) |BETA|External use, third-party preview, TW review|?|
|option (wix.api.exposure)|PUBLIC|?|Enable field in public preview and "live" docs|
|option (wix.api.exposure)|PRIVATE|?|HIDE field from public preview and "live" docs|

## Velo Doc issues
- [ ] naming
- [ ] comparison with REST
- [ ] p13n rules

# Release - TW

## REST Release
 - [ ] last TW read over
 - [ ] final review with REST team lead
 - [ ] set up scopes **create the scopes a few days before we want to expose**
  - [ ] Record in [spreadsheat](https://docs.google.com/spreadsheets/d/1FvbXWI4pPVVy2_xSmB8cQRoijcLJvNl3Bbki05xB_RA/edit#gid=0)

 - Scope ID: `SCOPE.DC-<VERTICAL>.<MANAGE|READ>-<SERVICE-NAME-HYPHENATED>`
 - Permissions included in scope: Take directly from internal draft docs, nest scopes where reused, e.g. MANAGE includes READ 
 - Description for DC: Follow pattern of previous
 - Domain: (AKA Vertical)
 - Description for App Market Consent: Follow pattern of previous

Normally we expect to have 2 scopes:
 - read
 - manage (includes read + all write permissions)

  - [ ] Add in [catalog](https://bo.wix.com/wow/permissions/permission-catalog)

> You need permissions for this: https://library.wix.com/kb/en/article/it-bot-eva#request-bo-permissions

> You also need this petri experiment switched on: `specs.EnableThunderboltRenderer`

Fill in:
 - Name
 - ID
 - Description - from "Description for DC" above
 - Domain
 - Level (SITE)
 - Used By (Dev-center)
 - Ownership tag - ignore
 - Contains - search by copy paste from spreadsheet for exact match


Final step to expose:

****isExternal****

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

## Wix Docs Backstage - release!

https://bo.wix.com/wix-docs-backstage/projects

## Announce

### Development Team!
Copy in the PM and share in the Slack channel for the whole team
### App Market
Post in #am-tw-chat with a short description of the API and its functionality
Tag Steve Kirk and Zachary Dinerstein (app market KB and newsletters) and Zachary Dinerstein (consent texts)
### PR the API description to the Docs Release Notes

 - [ ] add new API to https://github.com/wix-incubator/wix-rest-docs/blob/master/guides/ReleaseNotes.md
 - [ ] add any deprecated fields to https://github.com/wix-incubator/wix-rest-docs/blob/master/guides/Deprecations.md

### P13n
Post in #api-tpa-priorities
- Platformization board - https://wix.monday.com/boards/32755082
- Velo-TPA Doc Tasks board - https://wix.monday.com/boards/97005963/

#### Archive

Spreadsheet or other format reviews.


# Use case template

//todo: add brief introduction of the product

# About the \<XXX\> API

<!---  
A description of the full API
--->

Wix Things creates a catalog of things and allows site owners to create smaller collections of things by type or other attribute. A catalog organizes the site’s products and collections and facilitates doing stuff with things. With the Wix Things Catalog APIs you can query individual things, collections or the entire catalog, as well as create things and add their unique stuff.


## Terminology
<!---
List of all main entities (objects) addressed by the API, and their relationships to each other.
--->

- **Catalog**: A single, complete list of all the sites’s things. Compiled automatically.
- **Collections**: Themed groupings of things for stuff that a site owner can create to organize their whatever. Things can belong to multiple collections, but each collection may appear only once in the whole catalog. </br>


## Understanding X, Y, Z...

<!--- notes on any especially complex entity or relationship needed to work with the API --->

## Examples

<!--- examples of more complex entities if needed --->

## Limitations

	- Things can be automatically populated with stuff, but each bit of stuff needs to be added manually by a site member with the permissions or whatever.
	- Things have to be in places. Stuff can be nowhere though.

## Integrations

<!--- other Wix apps that the API interacts indirectly with --->
