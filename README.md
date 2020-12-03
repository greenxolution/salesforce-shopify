# GUIJE Salesforce - Shopify Integrator

- The customers are automatically added to Salesforce after they've completed their first order online or were added to Shopify.
- Any customer changes automatically update in Salesforce.
- The orders are added to Salesforce after were created in Shopify.
- You can customize the process and logic easily. It's an unmanaged package; you have access to the code and flows once it's installed.
- This version is free.

**Shopify Requirements:**
Create a Private app that allows access to your data through the API.

**Salesforce Requirements:**
Create a force.com site in your Salesforce (see the documentation)
Install the GUIJE Salesforce - Shopify application.

[![homepage][1]][2]

[1]:  caswota_video_cover.png
[2]:  https://www.youtube.com/watch?v=qA_KkpOrGh0=emb_logo

# Installation
GUIJE Salesforce - Shopify v1.4  link [click here](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t3i000002imDfAAI "GUIJE Salesforce - Shopify")

## Configuration Steps


![](https://github.com/greenxolutions/guije-shopify/blob/master/images/ShopifyCreateForm.png?raw=true)

Screen Details:

**Information**

|  Field Name  | Comments  |
| ------------ | ------------ |
| Store Name  | It could be your Shopify Store name |
|  Salesforce site URL  |  The site created in your SF org. See: Create Salesforce site |

**Shopify Private Apps**

|  Field Name   | Comments  |
| ------------ | ------------ |
|  API Key  |    |   
| Password | | 
| Example URL ||
| Shared Secret ||
| Storefront access token |||

**Webhook (read only)** It's a security SHA value. It's read only.

**Synchronization Options**

|  Field Name   | Comments  |
| ------------ | ------------ |
| Import Customer | The customer data is sent to Salesforce when the customer is created and edit |
| Import Order | The order data is sent to Salesforce when the order is created |

**Source of data**
The data are taken from the Shopify custom app (see https://shopify.dev/concepts/apps)
![](https://github.com/greenxolutions/guije-shopify/blob/master/images/ShopifyAppData.png?raw=true)

## Salesforce Admin Tasks after intalling:
**Add Salesforce Sites.**
The communication from Shopify to Salesforce is through Shopify Webhooks. For this reason, the GUIJE package has Web Services. The Public Access Settings must include the following classes in the "Enabled Apex Class Access" option.
- GUIJE_Shopify_Action_ParseJSON
- GUIJE_Shopify_WS

**Remote Site Settings.**

Add a remote site with your Shopify URL.


