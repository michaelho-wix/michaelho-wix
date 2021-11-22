## Velo examples

You can put comments in the response object like in normal JS code. meaning /**/ and // will work here.
For example:
{"purchases": [{                   /* Your Comment */
  "productId": "mid-tier",        // Your Comment
  "price": "0",
  "currency": "USD",
  "billingCycle": "YEARLY",
  "dateCreated": "2020-07-21T08:45:18Z"
}]}

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

https://docs.google.com/document/d/1D2B8PHPZ9DhqrDkGBKZgguiH4gFm5PHoajjnBu67G9g/edit#heading=h.1w3ewziaufiv

<hr>

---
sidebar_position: 1
---

# Process Overview

[Decision tree for exposing REST APIs](https://miro.com/welcomeonboard/aTBQRHYxZFdybkt1TmlGc0NHRHJJOXJDZVpwb1lFOW9ucFlib0VmUWdOb2FMY3JzcmNjSmd1ZnhZcmlvempVTXwzMDc0NDU3MzU1NDQxMDIwOTkz) (WORK IN PROGRESS)

<hr>

<!-----
NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 0.635 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β31
* Tue Oct 26 2021 23:26:24 GMT-0700 (PDT)
* Source doc: API Spec - Draft
----->


Terminology in this doc:


# API SPEC


## General Data

**Vertical:** e.g., Wix Stores

**API Name:** e.g., Catalog


# **Description:** e.g., Wix Stores creates a catalog of store owners’ items for purchase and allows store owners to create smaller collections of products by type or theme. A catalog organizes the store’s products and collections and facilitates inventory management. With the Wix Stores Catalog API you can query individual products, collections or the entire catalog, as well as create products and add their media.

**Terminology:**  	



* Catalog = a complete list of all the store’s products - compiled automatically.
* Collections = themed groupings of items for purchase that a store owner can create to organize their products (e.g., Spring 2019, Running shoes, etc.). Products can belong to multiple collections.

 \
	**Limitations:**



* Price discounts for collections apply to every item in that collection, no matter the item's price. If the coupon sets a $10 discount and there is an $8 item in that collection, that item will be free when a customer applies the coupon code.
* Coupon codes are case and space sensitive. (We recommend instructing customers to copy and paste the coupon code without making any changes.)

See [Intro Examples](https://docs.google.com/document/d/18TDU40kPEmVxHNJ5AFNPo82DDgPv5uLIYGeOiGJFLjI/edit?usp=sharing) for more details.

**Real-Life Business Scenarios:** 


    **TPA**: e.g., Coordinate a store’s inventory across other sales platforms (e.g., Facebook marketplace), or inventory management tools (e.g., NetSuite, TradeGecko).

**Use Cases:**


    **TPA**: 	1. Query Products and populate database. 


        2. Sign up for Product Created/Changed/Deleted webhooks, and periodically call Query Products and filter by `lastUpdated`. 


    3. Create/Update/Delete Products as required.


     (Note: Every call will trigger a webhook)

See [Use Case Examples](https://docs.google.com/document/d/18TDU40kPEmVxHNJ5AFNPo82DDgPv5uLIYGeOiGJFLjI/edit?usp=sharing) for more details.

**Objects/Entities:** (link to proto?)


## Data Per Endpoint/API

**User Stories** (one or more steps in the Real-Life Scenario/Use Case)



1. Whenever possible, create 1 story that fits both platforms
    1. TPAs
        1. As a TPA, I want to sync a site’s products to my platform, including inventory status.
        2. As a TPA, I want to import my products to a site owner’s store and make them available for purchase.
    2. Corvid
        3. As a Corvid Dev, I want to list all currencies for which Wix supports conversion.
        4. As a Corvid Dev, I want to convert an array of one or more amounts from one currency to another and display them to my site visitor.

**Endpoints:**

**	Request URL + params + required/optional:**

**	Response/Returns: **


    **TPA: **Is it different from the object?


    **Corvid: **Full response. For promises, what does fulfilled and rejected mean?

**	Roles & Permissions: **

**		TPA Only**

** 	Errors:**

**		Error codes and descriptions:**


    **[Guidelines](https://www.google.com/url?q=https://bo.wix.com/wix-docs/rnd/platformization-guidelines/errors&sa=D&ust=1604322617619000&usg=AFQjCNHsCLCGxvPI3_ZCHagu34o_HCDjvQ)**

**	Code Sample:**

**		TPA:**


        Call in Curl with any relevant parameters


        Full JSON response


        **Corvid**: 


        	Simplest example of calling API and its return value


        	Use case using API 

<hr>

---
sidebar_position: 2
---

# REST API "definition of done" checklist

## Use cases

|criterion| definition | MUST / SHOULD ? |
|-| - | - |
| Introduction |Describe API (from the TPAs point of view)| MUST |
| Links | Help center articles to explain concepts | |
| Business case | Real-world value to site owner & site visitor (what is this? what is it for?)| MUST |
| Terminology | All API-specific terms (entities and their relationships) defined| MUST |
| Section introduction | Introduction to your vertical and what it does | M - if first of its vertical |
| Limitations | List of any limitations or “features” that may affect TPAs (for example, functionality that | |
| Use cases | End-to-end implementation of at least one basic TPA use case| |

## Implementation

|criterion| definition | MUST / SHOULD ? |
|-| - | - |
| Implementation example | Short description or steps for complete implementation including which requests to send| MUST |
| Parameter descriptions | Descriptions for all parameters| MUST |
| Filter and sort | Documentation for filter and sort capabilities| MUST |
| Dependencies | Features based on other verticals are actually supported | MUST |
| URL Slugs | No slug can be updated via API b/c of internal issues| |
 
## Documentation

|criterion| definition | MUST / SHOULD ? |
|-| - | - |
| Consistency | Same verbs & nouns used for requests, parameters, responses | MUST |
| Clarity | No identical endpoints; clear difference in name & use case per endpoint | MUST |
| Logic |  No contradictions in descriptions | MUST |
 | Endpoint use case | Endpoint names express what they do (VERB + NOUN + CONTEXT) | MUST |
| Enum defaults | 0 option is the default / unknown (???)| |
|Enum descriptions | All enum options are described |MUST|
| field masks| About field masks: https://dev.wix.com/api/rest/wix-bookings/bookings/patch-endpoints-and-field-masks-in-update-requests | |

## Security

|criterion| definition | MUST / SHOULD ? |
|-| - | - |
| 3rd party user access | Only parameters / stuff that 3rd party users can access | MUST |
| MSID |  Meta-site ID should not be requested explicitly, will be resolved from the accessToken by AGW)| |
| cookies | No user/member/visitor cookie required | MUST |
| Greyhound   | No links to internal resources | MUST |
| RPC | No links to internal resources | MUST |
| wix-private Github| No links to internal resources | MUST |
| Internal libraries| No links to internal resources | MUST |
| Google Sheets/Slides| No links to internal resources | MUST |
| API Permissions | Every endpoint and webhook must be protected by a permission| MUST |
| Multiple permissions | Only 1 permission per endpoint / webhook | |
| URL pattern | `<base>/<service>/v1/<resource-path>` | MUST |
| URL host in YAML |MUST|
| Code samples|  for each endpoint and webhook (+ object)| MUST |

## Publication (exposure)

|criterion| definition | MUST / SHOULD ? |
|-| - | - |
|TEST |When stable, test all the endpoints |MUST |
| Wix Docs annotation |  `Wix docs = true` | MUST |
| Exposure annotation |  `option (wix.api.exposure) = PUBLIC` | MUST |
| Parameter names |  per guidelines| MUST |
| Direct references to other parameters |  - should be nested| |
| Deprecated parameters |  `deprecated = true` and add an end-of-life date :-) and update deprecations plan | MUST |
| Required parameters |  (the default is optional!)| MUST |
|`INFERRED` annotation |[docs](https://github.com/wix-private/server-infra/blob/master/framework/grpc/p13n/auto-field-masks/README.md)|MUST|
| Read-only parameters | | |
| Irrelevant endpoints | Remove all (or mark as deprecated)| |
| Object|  (entities in YAML)| |



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
