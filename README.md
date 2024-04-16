
> ## Now available within Postman's API Network
> The Stripe API Collection is now hosted within [Stripe's public workspace](https://www.postman.com/stripedev/workspace/stripe-developers/overview) in Postman.  This means you no longer need to import this collection, but can instead fork from the public workspace into yours. Head over there to get started. 
## Stripe API Postman Collection
This is a postman collection covering the Stripe API. See https://stripe.com/docs/api for more details.
## Prerequisites
- [Postman](https://www.getpostman.com/downloads/)
- [Stripe Account](https://dashboard.stripe.com/register)
## Getting Started
To get started you can either fork the collection from [Stripe's public workspace](https://www.postman.com/stripedev/workspace/stripe-developers/overview) within Postman or import the collection JSON file from this repo. 
### Fork the collection from Stripe's public workspace
From within the [Stripe's public workspace](https://www.postman.com/stripedev/workspace/stripe-developers/overview), fork the Stripe API collection:

![Fork collection](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_fork_collection.png)

Enter a name for your fork and select the workspace where it will be created: 

![Fork form](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_fork_form.png)

You can also fork the environment template from the Stripe Developers Workspace:

![Fork environment template](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_fork_env_template.png) 

Next: [Set your API key](#set-your-api-key)
### Import the collection file into your workspace
If you don't want to fork the collection from the public workspace, you can import it from this repo. 

Within your Postman workspace select the Import button:

![Import collection](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_import_collection.png)

Next copy the [StripeAPICollection.json](https://github.com/stripe/stripe-postman/blob/master/StripeAPICollection.json) contents and paste in the **Paste Raw Text** section of the import dialog:

 ![Import raw text](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_import_raw_text.png)

### Set your API key
To run requests you'll need to supply your [testmode secret API key](https://dashboard.stripe.com/test/apikeys) and set it as an [environment variable](https://learning.postman.com/docs/sending-requests/variables/) within your workspace.

To set any environment variable, fork the environment template within the Stripe public workspace, or create a new envionment within Postman:

![create a new environment](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_create_new_env.png)

Add your secret key as a variable to the environment and save:

![set API key](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_set_key_and_save.png)

Set the environment to active:

![save as active](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_set_active_env.png)

Now within the collection set it to use the environment you just created:

![set collection environment](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_set_collection_environment.png)

If your environment is set up correctly, you should see your secret key value if you mouse over the `secret_key` variable in the Token field:

![secret key mouseover](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_secret_key_mouseover.png)



Be sure to save the collection after you've configured the set the key:

![save key](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_save_key.png)

## Make a test call
You should be ready now to make a test call. An easy first call is to create a customer:

![customer endpoints](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_customer_endpoints.png)

Since no parameters are required to create a customer, you can just hit the Send button to run this request:

![create customer send](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_create_customer_send.png)

If your environment is set up you'll get a customer object back as the response to the call:

![create customer send](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_customer_create_no_params_response.png)


Add parameters to the call by clicking the body tab, where you'll see a list of available parameters.  Select and populate the ones you want to use. Here's an example of adding an email parameter:

![create customer with email](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_create_customer_with_email_request.png)

You'll see the email address in the reponse:

![create customer with email](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_create_customer_with_email_response.png)

## Passing Metadata In a Request
Right now [metadata](https://stripe.com/docs/api/metadata) does not show up as a optional parameter on requests, but it can still be provided to calls that will accept it.  Here's an example of adding 2 metadata fields to the customer create call:

![set metadata on a request](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_set_metadata.png)

Metadata key value pairs can be updated in a similar manner. To remove a metadata key during an update call, supply the `metadata[key]` parameter without setting a value.  This will pass an empty string as part of the request:

![clear metadata key](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_update_metadata.png)

To remove all metadata pass the `metadata` parameter without a value set:

![remove metadata key](https://raw.github.com/stripe/stripe-postman/master/screenshots/postman_remove_metadata.png)

## Other useful links
- [Stripe API docs](https://docs.stripe.com/api)
- [Stripe Developers YouTube](https://www.youtube.com/stripedevelopers)

To keep track of major Stripe API updates and version, reference the [API upgrades page](https://docs.stripe.com/upgrades#api-versions) in our documentation. For a detailed list of API changes, please refer to our [API Changelog](https://docs.stripe.com/changelog).


## We want to hear from you
We want to hear how we can make the collection better! Don't hestiate to file [issues](https://github.com/stripe/stripe-postman/issues) for any bugs you encounters, features you'd like to see or other suggestions you have.
