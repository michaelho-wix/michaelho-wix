# Best practices

Aims:

 - help readers know what they don't know (but need to)
 - help readers find what they need to know
 - help readers understand what they need to understand, quickly and easily

## Three issues in tech comms

### Reference - what is "this"?

 - move from general to specific to **avoid getting lost in details and exceptions**, e.g.

The editor provides some JS automatically (apparently?) and Velo code adds some, this needs to be made explicit and very clear, as well as *when code specifically needs to be added and when not (at least typically)*

All Wix apps and editor elements use a manageably small set of user actions concepts such as adding elements, customizing them, creating and handling events, running functions on data, etc.

These could be called out more prominently and then referred to throughout the documentation to make it usable.

 The examples used below for DRY versus WET writing contain more basic use cases that could apply to any website:

 - Querying collections
 - Get data from specific apps
 - Determine the type of device the site is being viewed on
 - Pass information between pages
 - Store data selected by the site user
 - Store information retrieved from collections
 - Map data so they can be easily accessed by ID
 - Create a status flag 

These can then be used for e.g.
 - Section headers to navigate articles
 - Links to related how-to and what-is articles
 - Common use cases to re-use text within and across articles

 - link to definitive, technical sources e.g.

#### Instead of a blog post

https://codeburst.io/javascript-es-2017-learn-async-await-by-example-48acc58bad65

#### Maybe this developer doc

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await

 - put code annotations right inside the code
   - comments
   - side-by-side

### Logic - how does it work?

 - topic-based writing AKA modular writing AKA DRY ;-)
   - break down longer articles into chunks and explain what each part is doing e.g.

https://support.wix.com/en/article/velo-tutorial-creating-a-bookings-timetable

### Relevance - why does this apply to me, now?

 - Don't over-describe. You could potentially describe everything in the universe as background to any given task. The rule is: if it's already described somewhere else, don't include it. If a product uses commonly-understood systems, don't describe them again, or at most briefly mention that they are used. Otherwise this becomes filler text, which robs reader attention. If there are large numbers of relevant exceptions or cases, try to group these and generalize, and then move the lists of specfics to a separate topic.

 - links to relevant articles / tutorials / reference examples

 - use fewer words, delete filler words, because they are not relevant to the user trying to complete an action

 - findability
   - DRY (don't repeat yourself) because WET (writing everything twice) uses extra thinking time / energy to answer the question, "what am I looking at and what am I looking for?"
   - include sign-posts to show the reader where to look and what to look for:

#### Before - lots of repetition, both of concepts ("Import the...") and of filler words ("which is used for...")

Line 1: Import the wix-data module, which is used for querying the Bookings collections.
Line 2: Import the wix-bookings module, which is used to get the available service slots.
Line 3: Import the wix-window module, which is used to determine the type of device the site is being viewed on.
Line 4: Import session storage from the wix-storage module, which is used to pass information between pages.

Line 6: Create a variable to store the selected day for which to show classes.
Line 7: Create a map to store the staff member information retrieved from the Staff collection.
Line 8: Create a map to store the services so they can be easily accessed by ID.
Line 9: Create an array to store the list of services retrieved from the services collection.
Line 10: Create a flag that indicates whether the site is being viewed on a mobile device.

#### After - this could be a point to link to the common use cases mentioned above in "general to specific"

Here is that code, line-by-line:

Imports

1: Wix-data module, queries the Bookings collections.
2: Wix-bookings module, gets the available service slots.
3: Wix-window module, determines the type of device the site is being viewed on.
4: Session storage (from the wix-storage module), passes information between pages.

Variables

6: string: selected day for which to show classes.
7: map: staff member information retrieved from the Staff collection.
8: map: services for easy access by ID.
9: array: list of services retrieved from the services collection.
10: flag: set to true if the site is being viewed on a mobile device.
