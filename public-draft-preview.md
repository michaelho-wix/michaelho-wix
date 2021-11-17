# Sharing ALPHA API with 3rd Party

The following article will explain how you can share your API Documentation at an early stage while still in ALPHA. You will be able to generate a ***shareable private link***, only those with the link can view your API Documentation - it will not be available publicly to all 3rd party developers.

This process is relevant only to collect feedback from a specific TPA. The TPA must be aware that the API will break or change without notice and that it is not ready yet for consumers.

If your API is ready to be fully exposed to 3rd Party, you should not use the following guidelines, but rather read the full guidelines for [Exposing APIs to 3rd Party](./exposing-to-3rd-party.md).

> **Notes**:  
> - This solution should be known and approved by the relevant person in the company such as Biz Dev, PM, etc.  
> - This link is permanent, however the content of the API is automatically updated whenever the developer changes the proto. 

### Guidelines:
1. Make sure that the proto service is marked with the following:
   1. Exposure: PUBLIC
   1. Maturity: ALPHA
1. Make sure that a technical writer has reviewed the API use case. Fill out [this template](https://docs.google.com/document/d/1l4Z8cV1ddQdp5apP82j-yMzDExoQBxd0iV0ZuZl7T4Q/edit?usp=sharing) for every relevant use-case. (Major naming issues will probably be caught at this stage, but the TW review can’t be considered complete, and there will almost certainly be more changes required before the API can go public.)
1. Once the above are done and the API is merged into master, an **automatic** version of the API will be created under the following private link: `https://dev.wix.com/api/rest?branch={api-name}`  
   > **Note**:  
   > `api-name` = the title in the documentation.yaml. For example, the “Wix Stores Orders” API is ready, the link will be: `https://dev.wix.com/api/rest?branch=wix-stores-orders`

1. **Category in Wix Docs** - by default, your new API will be listed under the **Drafts** category.
