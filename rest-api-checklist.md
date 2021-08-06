# REST API definition of done

Check each box when the condition is true.

## Check quality

 - [ ] Introduction to the API (from the TPAs point of view)
   - [ ] Short introduction (what is this? what is it for?)
   - [ ]  all terminology
   - [ ] (Only if the vertical doesn’t have exposed docs yet) Introduction to your vertical and what types of TPAs can work with it
   - [ ] List of any limitations or “features” that may affect TPAs (for example, functionality that is different from your competitors, that TPAs should be aware of when building an app that manages the site owner’s offering in both Wix and a competitor’s platform)
- [ ] Descriptions for all parameters
- [ ] Documentation for filter and sort capabilities

- [ ] API must support the end-to-end implementation of at least one basic TPA use case
- [ ] Consistency (if the Join Waitlist endpoint returns a `registrationId`, chances are the endpoint should be called “Register to Waitlist”)
- [ ] Clarity of use (per endpoint) - will the TPA understand within 3 seconds what they can do with the endpoint? (Naming is crucial here)
- [ ] Multiple similar-sounding endpoints - require extra details to clarify the difference, when relevant consider only exposing 1
- [ ] Clarity in all texts/descriptions - nothing like this one:
- [ ] “Associating a service with a category is optional. However, currently in Wix XXX a category must be defined for each service created.”
- [ ] Look out for any functionality that is based on other verticals - must make sure that the other vertical supports the functionality (often it doesn’t)


## Remove blocks

- [ ] Wix Docs annotation (Wix docs = true)
 - [ ] Exposure annotation option (wix.api.exposure) = PUBLIC
 - [ ] Parameters/stuff that 3rd party users can’t access:
 - [ ] MSID (should not be requested explicitly, will be resolved from the accessToken by AGW)
 - [ ] User/member/visitor cookie 
 - [ ] Any internal tools: 
 - [ ] Greyhound 	
 - [ ] RPC 
 - [ ] wix-private Github
 - [ ] Internal libraries
 - [ ] Links to Google Sheets/Slides
 - [ ] URL as per guidelines - (host in YAML)
 - [ ] Code samples for each endpoint and webhook (+ object)
 - [ ] Parameter names as per guidelines
 - [ ] Parameters that are referring directly to other parameters - should be nested
 - [ ] Mark any/all deprecated parameters (deprecated = true)
 - [ ] Mark any/all required parameters
 - [ ] Mark any/all read-only parameters
 - [ ] Remove any/all irrelevant endpoints (or mark as deprecated)
 - [ ] Object (entities in YAML)
 - [ ] Every endpoint and webhook must be protected by a permission
 - [ ] Multiple permissions for 1 endpoint or webhook are a red flag - talk to Aliza ASAP
