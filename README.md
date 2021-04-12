## Stripe API Postman Collection

This is a postman collection covering the Stripe API. See https://stripe.com/docs/api for more details.

## Getting Started

### Fork the collection

Get started by forking the collection into your private workspace:

![fork](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_fork_collection.png)

### Set your API key

To run requests you'll need to supply your [testmode secret API key](https://dashboard.stripe.com/test/apikeys) and set it as an [environment variable](https://learning.postman.com/docs/sending-requests/variables/) within your workspace.

To set any environment variable, create a new envionment within Postman:

![create a new environment](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_create_new_env.png)

Add your secret key as a variable to the environment and save:

![set API key](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_set_key_and_save.png)

Set the environment to active:

![save as active](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_set_active_env.png)

Now within the collection set it to use the environment you just created:

![set collection environment](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_set_collection_environment.png)

If your environment is set up correctly, you should see your secret key value if you mouse over the `secret_key` variable in the Token field:

![secret key mouseover](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_secret_key_mouseover.png)

Be sure to save the collection after you've configured the set the key:

![save key](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_save_key.png)

## Make a test call

You should be ready now to make a test call. An easy first call is to create a customer:

![customer endpoints](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_customer_endpoints.png)

Since no parameters are required to create a customer, you can just hit the Send button to run this request:

![create customer send](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_create_customer_send.png)

If your environment is set up you'll get a customer object back as the response to the call:

![create customer send](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_customer_create_no_params_response.png)

Add parameters to the call by clicking the body tab, where you'll see a list of available parameters. Select and populate the ones you want to use. Here's an example of adding an email parameter:

![create customer with email](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_create_customer_with_email_request.png)

You'll see the email address in the reponse:

![create customer with email](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_create_customer_with_email_response.png)

## Passing Metadata In a Request

Right now [metadata](https://stripe.com/docs/api/metadata) does not show up as a optional parameter on requests, but it can still be provided to calls that will accept it. Here's an example of adding 2 metadata fields to the customer create call:

![set metadata on a request](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_set_metadata.png)

Metadata key value pairs can be updated in a similar manner. To remove a metadata key during an update call, supply the `metadata[key]` parameter without setting a value. This will pass an empty string as part of the request:

![clear metadata key](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_update_metadata.png)

To remove all metadata pass the `metadata` parameter without a value set:

![remove metadata key](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_remove_metadata.png)

## Changelog

### 03-23-21

API Changes:

- Added support for the [Billing Customer Portal](https://stripe.com/docs/api/customer_portal)
- Added [AfterPay/ClearPay as a Payment Method](https://stripe.com/docs/api/payment_methods/create#create_payment_method-afterpay_clearpay)
- Added [`on_behalf_of`](https://stripe.com/docs/api/invoices/create#create_invoice-on_behalf_of) parameter for Invoices. See [Invoices with Connect](https://stripe.com/docs/billing/invoices/connect) for more documentation.

Generation changes (for internal use during beta, we won't include this once the collection is public)

- Generated with the official postman converter instead of our fork, as the bug we filed around required parameters has been fixed.

### 03-17-21:

Initial collection

## Get Support

Please reach out to @dawn or to the [#proj-da-postman-collection channel](https://app.slack.com/client/T024F4A92/C01REK7PNNA/details/top)

## We want to hear from you

Please fill out the [feedback doc](https://paper.dropbox.com/doc/Postman-collection-internal-feedback--BHjTBMKgyATmftHWF0SfTpULAg-fvt4yO5616kEZmoIpuWz2)
