# REST API definition of done

Check each box when the condition is true.

## Check doc quality

 - [ ] Introduction to the API (from the TPAs point of view)
   - [ ] Short description (what is this? what is it for?)
   - [ ]  All specific terminology is defined
   - [ ] (Only if the vertical doesn’t have exposed docs yet) Introduction to your vertical and what types of TPAs can work with it
   - [ ] List of any limitations or “features” that may affect TPAs (for example, functionality that is different from your competitors, that TPAs should be aware of when building an app that manages the site owner’s offering in both Wix and a competitor’s platform)
   - [ ] API must support the end-to-end implementation of at least one basic TPA use case
     - [ ] Short description OR
     - [ ] Steps for complete implementation including which requests to send
- [ ] Descriptions for all parameters
- [ ] Documentation for filter and sort capabilities

## Check design / usability 

- [ ] Consistency with use cases:
  - [ ] Look out for any functionality that is based on other verticals - must make sure that the other vertical supports the functionality (often it doesn’t)
  - [ ] Consistency (if the Join Waitlist endpoint returns a `registrationId`, chances are the endpoint should be called “Register to Waitlist”)
  - [ ] Multiple similar-sounding endpoints - require extra details to clarify the difference, when relevant consider only exposing 1
- [ ] Clarity in all texts/descriptions:
  - [ ] No contradictories e.g. “Associating a service with a category is optional. However, currently in Wix XXX a category must be defined for each service created.”
  - [ ]  Clarity of use (per endpoint) - will the TPA understand within 3 seconds what they can do with the endpoint? (Naming is crucial here)


## Remove blocks to exposure

- [ ] Wix Docs annotation (Wix docs = true)
 - [ ] Exposure annotation option (wix.api.exposure) = PUBLIC
 - [ ] Parameters/stuff that 3rd party users can’t access:
 - [ ] MSID (should not be requested explicitly, will be resolved from the accessToken by AGW)
 - [ ] User/member/visitor cookie 
 - [ ] No links or references to internal tools: 
   - [ ] Greyhound 	
   - [ ] RPC 
   - [ ] wix-private Github
   - [ ] Internal libraries
   - [ ] Links to Google Sheets/Slides
 - [ ] URL as per guidelines - (host in YAML)
 - [ ] Code samples for each endpoint and webhook (+ object)
 - [ ] All parameters are marked and set correctly:
   - [ ] Names as per guidelines
   - [ ] Direct references to other parameters - should be nested
   - [ ] Deprecated (deprecated = true)
   - [ ] Required (the default is optional!)
   - [ ] Read-only
 - [ ] Remove any/all irrelevant endpoints (or mark as deprecated)
 - [ ] Object (entities in YAML)
 - [ ] Permissions:
   - [ ] Every endpoint and webhook must be protected by a permission
   - [ ] Multiple permissions for 1 endpoint or webhook are a red flag - talk to Aliza ASAP

<?--- based on https://docs.google.com/document/d/1hhQrnA07TMjYaX_c05mHRf5jjqtDSSFrxlzfMZ93xdA/edit?userstoinvite=laurake%40wix.com&actionButton=1# --->
