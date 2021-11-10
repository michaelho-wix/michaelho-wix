## Public REST Doc preview

**WHY?** To see the doc as it will appear as a finished product to the world 🙂

- From the internal ("bo.wix.com") doc, click on one of the articles, then the "view source" button to get into the API's repo
- Find `documentation.yaml` in your API's repo (work your way through the breadcrumbs / repo folder structure at the top of the screen, and see what files are in each folder. Normally it's kept under "proto")
- Make the title of the overall doc into a URL slug, e.g. for:

```yaml
apiDoc:
  title: Wix Blah
```
The slug will be `wix-blah`

- Add the slug into the following URL pattern:

```
https://dev.wix.com/api/rest/drafts/wix-blah?branch=wix-blah
```

**WARNING** Replace the `drafts` part of the routing with `wix-blah` when using this URL in the docs themselves.


<hr>

# Expose a rest API
1. Use [the internal REST & RPC menu editor](https://bo.wix.com/wix-docs-backstage/projects/519ba616-bc00-43a6-b7d4-c333fc87cd1e/sites/dfd344c3-ecd3-404b-8282-5486786c6cd0/menu-editor) to move the docs out of draft
1. Expose scopes to dev center
 - write in [Excel sheet](https://docs.google.com/spreadsheets/d/1FvbXWI4pPVVy2_xSmB8cQRoijcLJvNl3Bbki05xB_RA/)
 - https://bo.wix.com/wow/permissions/manage-scope
3. expose webhooks to dev center
4. expose documentation
5. notify #am-tw-chat and #api-tpa-priorities


## Generate a local preview

## View a Public Draft


`https://dev.wix.com/api/rest?branch=<branch-name>`


<hr>

https://bo.wix.com/wow/permissions

scopes catalog https://bo.wix.com/wow/permissions/scope-catalog

scope IDs listing: https://docs.google.com/spreadsheets/d/1FvbXWI4pPVVy2_xSmB8cQRoijcLJvNl3Bbki05xB_RA/edit?usp=sharing

check correct permissions 

check able to expose
disable specs.EnableThunderboltRenderer in petri

log into wix.com/dc3/myapps

expose

go into dev centre with a non-wix email to check scopes externally exposed


https://bo.wix.com/wix-docs-backstage

in public viewer, find relevant branch

review & merge! :)

menu manager

put in CRUD order
