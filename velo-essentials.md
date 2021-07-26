# The Essentials of Velo

_A guide for the perplexed_

## What happens when a page loads into a browser

1. Site's onReady()
2. Page's onReady()

## What happens when a user interacts with a page

3. Element's onReady()

 set up default content

4. Element's events
 - set up variables
 - query collections
 - set element's data
 - populate element's contained elements

Basic Concepts

Page elements
 - issues with specific types of elements
   - container boxes
     - hold other elements to group them together
     - add elements to the group by dragging & dropping; when "attach to box" appears, drop into the desired place
     - WARNING: there is no feedback to inform user that the element has been attached
     - INFO: try moving the container box and see if the elements you tried to attach move with it(!)
 - properties
 - methods
 - event handlers
 - references

 $w() selects by
  - name (add the # before the literal name), and
  - type (no # needed)

"Mixins" - shared page element properties / functions (?)

Import function

Export function

Promises

Callbacks

Data arrays

 - Built-in objects by vertical
 - 

Previewing & debugging code

 - using console.log() to output elements' data
 - using .catch()
 ```.js
 .catch((error) => {console.error("hi!", error)});
 ```

Common Tasks


## Adding elements
## Customizing them
## Creating and handling events

### onReady

### onItemReady

## Running functions on data

Certification topics

$w Selector

Data / Content Manager

Data Connections

Dataset Element

Dynamic Pages

HTTP-Functions

Repeaters

Collection Permissions

NPM Modules

Backend and .JSW files

Job Scheduler

Site Monitoring

wix-fetch module

wix-data module

wix-storage module

wix-location module

wix-window module

Secrets Manager

In the following backend file, what does this function return?



Error: You cannot have a backend file with the .jsw extension.

Error: wixLocation cannot be used in the backend

Error: baseUrl is not a wixLocation property. Use wixWindow instead.

String: For Premium site: "https://domain.com/" For Free site: "https://user.wix-sites.com/"
2.

Which of the following is NOT a valid $w('Button') event?



onClick()

onChange()

onDblClick()

onViewportEnter()
3.

How do you determine what type of device a visitor is using to view your site?



Use wixWindow.formFactor.

Use the page's width to calculate the device type.

You cannot know what type of device is being used.

Use wixWindow.mediaQuery.
4.

Which frontend module and function navigate the user to another web page?



wixLocation.url()

wixLocation.to()

wixRouter.routeTo()

wixLocation.routeTo()
5.

What are Velo Packages?



Code libraries built with Velo that allow you to add specific functionality to your site.

Packages of swag sent to newly certified Velo developers.

Packages in the NPM registry that are approved to be used with Velo.

Requests sent by the client to trigger an action on the server.
6.

What is the difference between a collapsed element and a hidden element?



A collpased element will be removed from the DOM while a hidden element will have its display set to none.

A collapsed element will be hidden with an animation effect.

A collapsed element will not occupy any space on the page, while a hidden element will occupy the same space the element occupies when it isn't hidden.

A hidden element will still have a visible border while a collapsed element will not.
7.

Which of the following uses of $w is NOT valid?



$w('#itemID1, #itemID2, #itemIDt3')

$w('Button')

$w('.itemClass')

$w('#itemID')
8.

When setting up a database collection, what is the “Site Content” collection type?



An option in the permissions settings that sets the collection to “Read-only” or “Write-only”.

A predefined permissions template set so anyone can read the collection data. However, only the admin can create, update and delete the data.

An option in the permissions settings for connecting elements to a dataset.

A predefined permissions template set so that only site members can read, create, update and delete the collection data.
9.

How do you insert a record into a collection where the collection's "Create Permissions" are set to only the "Admin"?



It can only be done with a connected dataset which is set to the 'Write-only' mode.

It can't be done. The only way is to set the collection's "Create Permissions" to "Anyone".

By adding {supressAuth: true} to the insert operation when performed from the backend.

By adding {force: true} to the insert operation when performed in the backend.
10.

Which of the following are not valid field types in a Wix collection?



Single Option Selection, Multiple Options Selection

Reference, Multiple Reference

Date and Time, Time

Image, Media Gallery, Audio, Video
11.

To create a form for adding a new item to a database collection using a dataset, which of the following dataset modes should be used?



Write-only mode

Insert-only mode

Insert & Write mode

Read & Write mode
12.

To present data in the repeater using a dataset, which of the following dataset modes should be used?



Get-only mode

Read-only mode

Get & Read mode

Read & Write mode
13.

How do you send a POST request using wix-fetch?



Define POST as the method in the fetch options.

wix-fetch is only for GET requests. You need to use wix-send instead.

No need to. POST is already the default method when using wix-fetch.

Use wix-fetch in the backend, and then it defaults to POST.
14.

Which of the following statements about a repeater connected to a dataset are correct? Select all answers that apply.






15.

In which of the following cases will the beforeInsert data hook run?



When inserting a new item in the Content Manager.

When inserting a new item using a dataset.

When inserting a new item using the wix-data API.

All of the above.
16.

When will a repeater that is connected to a dataset display new content?






17.

Where can installed npm modules be used?



From backend files and frontend files.

From any frontend file, but not from backend files.

From any backend files, but not from frontend files.

It depends on where you installed the specific module.
18.

You have 6 items in a collection. Consider the following query:

wixData.query('News')
    .lt('wordCount', 5000)
    .eq('reporterName', 'Jason')
    .find()

Which items will appear in the query results?



Item with title: News Title 06

Items with title: News Title 06, News Title 01

Items with title: News Title 06, News Title 04, News Title 03

Item with title: News Title 01
19.

Which of the following methods can be used to transfer the value of a String variable (myVar) when navigating to a different page in your Velo app? Select all answers that apply.






20.

Which of the following is NOT a scheduling option when scheduling a recurring job?



Once a week.

Each full moon.

Once a day.

Twice a day.

