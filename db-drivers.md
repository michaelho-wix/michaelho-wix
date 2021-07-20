# DB Drivers ("Velo Wix ___ Collection Fields")

## Find the DB Driver

## Add your site to Guinea pig

https://bo.wix.com/petri/

 - search for experiment
 - edit experiment
 - filter by your site's meta-site ID
 - save changes

(Meta site ID is found in the URL of your site when you're logged into Wix.com)

## Review naming

## Review descriptions

## Review technical properties

 - You have to actually test each property by hand
   - (e.g. try to connect to data)
   - “Can use in dynamic page URL” need to create dynamic pages
 - Check if DB driver has hidden Created Date (createdDate) and Updated Date (\_updatedDate) fields? Most DB drivers do.
 - Include properties even if empty (value "no")
### How to test each property

 - Description
 - Type
 - Can connect to data
 - Can use in dynamic page URL
 - Read-only
 - Can be filtered
 - Can be sorted

### Mandatory fields:

https://support.wix.com/en/article/about-your-content-collection-fields#system-fields

## Send to Dev for Final review

Make sure Hidden label applied to the article, so only people with a direct URL will be able to view it (hidden from Wix help center and google).

Press publish button and send link to Dev

## Publish

 When you’re ready to publish, remove Hidden label

## Send to translations

 - only PT!

## Announce

 - If the published change is significant (new or updated API, not just a bug fix), in the Monday pulse, make sure that there is a summary of the release/change in the pulse update with a link to the documentation:

**Wix <VERTICAL>: New "<DB DRIVER>" Collection**
Alongside <OTHER DB DRIVERS>, and other <VERTICAL> collections, <DB DRIVER> are now available for access and query using Velo (Wix Data API) or the Content Manager.

<DB DRIVER> are <DESCRIPTION OF DB DRIVER>, and until now they were only accessible per <ENTITY OF DB DRIVER>. The new <DB DRIVER> collection includes all of a site's <DB DRIVER>. 

Learn more about the new Wix <VERTICAL> "<DB DRIVER>" Collection: <LINK TO NEW DB DRIVER ARTICLE IN WIX ANSWERS>

 - Then change the Notify status to Done.
 - Update the Date in the Monday pulse to today’s date.
 - Move the Velo Doc Tasks Monday pulse to Published on the Velo Doc Tasks board.

## Answers Article

<https://support.wix.com/en/article/working-with-wix-app-collections-77233>
