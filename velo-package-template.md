TODO:

- [ ] include returns in the syntax statement (if the function returns something)
- [ ] include the type of each parameter in the syntax statement
- [ ] list parameter descriptions after each function
- [ ] Add a description of the return under the parameters
You can use this readme as an example: https://github.com/wix-private/velo-package-readmes/blob/master/google-drive-integration.md

<!-- Output copied to clipboard! -->

<!-----
NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 0.49 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β29
* Tue Jun 15 2021 03:58:36 GMT-0700 (PDT)
* Source doc: Copy of Velo Package README template
----->



[TOC]



[TOC]



## Please duplicate the template below {#please-duplicate-the-template-below}


## &lt;Package Name> {#<package-name>}

&lt;A short paragraph explaining what the package does.>


### Setup {#setup}

Before using the package, set up the following:


#### &lt;3rd-Party Integration> Platform {#<3rd-party-integration>-platform}



1. &lt;If the package includes a 3rd-party integration, provide step by step instructions on how access the information required from the 3rd-party to set up the integration.>


#### Wix Platform {#wix-platform}


##### Secrets Manager  {#secrets-manager}



*   &lt;List any secrets required by the package that should be saved in the Secrets Manager.>


##### &lt;Wix App Dependencies> {#<wix-app-dependencies>}



*   &lt;List any Wix Apps required by the package. For example, Wix Stores or Member’s Area.>


##### Configurations {#configurations}



*   &lt;List any other actions or instructions required for setting up the package before use.>


### Package Content {#package-content}

This package includes a number of &lt;backend and/or public> files. To use the functions in the files in your backend/page/public code, import them with the following syntax:

import { &lt;functionName> } from '@velo/&lt;package name>’ 

OR if the file is on the backend: 

import { &lt;functionName> } from '@velo/&lt;package name-backend>’

 \
config.json

(If the package contains a config.json file)

The code in this editable file contains the configurations for &lt;list what the configurations define>. Follow the instructions in the [Setup](#setup) section to set up the configurations. 


#### &lt;package file1> {#<package-file1>}

&lt;A sentence or two describing the contents of the file.>

To use the functions below in your code, import them with the following syntax:


```
import { <functionName> } from '@velo/<package-name>' OR '@velo/<package-name-backend>';

```



*   &lt;Exposed exported function>

    &lt;A sentence describing the function and what it does.> 


    ```
    `export async function <functionName>`

    ```



#### &lt;package file2> {#<package-file2>}

To use the functions below in your code, import them with the following syntax:


```
import { <functionName> } from '@velo/<package-name/package-name-backend>';
```


&lt;A sentence or two describing the contents of the file.>



*   &lt;Exposed exported function>

    &lt;A sentence describing the function and what it does.> 


    ```
    export async function <functionName>

    ```



#### &lt;events.js> {#<events-js>}

(If the package includes an events.js file, describe the events in the file.) 



*   &lt;Event function>

    &lt;A sentence describing the function and what it does.> 


    ```
    export async function <functionName>

    ```



### How to Use the Package - optional  {#how-to-use-the-package-optional}

This section demonstrates how you can work with the package.

&lt;Demonstrate how to implement the main use case(s) for the package. List page elements if relevant and run through the code the user needs to add to their site. See existing readmes to get an idea of how to document this section.>


### npm Packages {#npm-packages}

This Velo package uses the following npm package(s). To view the npm license, see the npm readme.



*   &lt;List the npm package(s) used in the package and a embed a link to that npm package’s readme file.>


### Release Notes {#release-notes}

&lt;Version number of the released package, and a few words describing the package’s version.>


### Tags - will be written by the tech writer {#tags-will-be-written-by-the-tech-writer}

&lt;List one word tags separated by commas relating to the package. This will help developers to easily find the package they are looking for.>
