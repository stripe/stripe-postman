
> ## Now available within Postman's API Network
> The Stripe API Collection is now hosted within [Stripe's public workspace](https://www.postman.com/stripedev/workspace/stripe-developers/overview) in Postman.  This means you no longer need to import this collection, but can instead fork from the public workspace into yours. Head over there to get started. 
## Stripe API Postman Collection
This is a postman collection covering the Stripe API. See https://stripe.com/docs/api for more details.
## Prerequisites
[Postman](https://www.getpostman.com/downloads/)

[Stripe Account](https://dashboard.stripe.com/register)
## Getting Started
To get started you can either fork the collction from [Stripe's public workspace](https://www.postman.com/stripedev/workspace/stripe-developers/overview) within Postman or import the collection JSON file from this repo. 
### Fork the collection from Stripe's public workspace
From within the [Stripe's public workspace](https://www.postman.com/stripedev/workspace/stripe-developers/overview), fork the Stripe API collection:

![Fork collection](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_fork_collection.png)

Enter a name for your fork and select the workspace where it will be created: 

![Fork form](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_fork_form.png)

You can also fork the environment template from the Stripe Developers Workspace:

![Fork environment template](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_fork_env_template.png) 

Next: [Set your API key](#set-your-api-key)
### Import the collection file into your workspace
If you don't want to fork the collection from the public workspace, you can import it from this repo. 

Within your Postman workspace select the Import button:

![Import collection](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_import_collection.png)

Next copy the [StripeAPICollection.json](https://github.com/stripe/stripe-postman/blob/master/StripeAPICollection.json) contents and paste in the **Paste Raw Text** section of the import dialog:

 ![Import raw text](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_import_raw_text.png)

### Set your API key
To run requests you'll need to supply your [testmode secret API key](https://dashboard.stripe.com/test/apikeys) and set it as an [environment variable](https://learning.postman.com/docs/sending-requests/variables/) within your workspace.

To set any environment variable, fork the environment template within the Stripe public workspace, or create a new envionment within Postman:

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


Add parameters to the call by clicking the body tab, where you'll see a list of available parameters.  Select and populate the ones you want to use. Here's an example of adding an email parameter:

![create customer with email](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_create_customer_with_email_request.png)

You'll see the email address in the reponse:

![create customer with email](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_create_customer_with_email_response.png)

## Passing Metadata In a Request
Right now [metadata](https://stripe.com/docs/api/metadata) does not show up as a optional parameter on requests, but it can still be provided to calls that will accept it.  Here's an example of adding 2 metadata fields to the customer create call:

![set metadata on a request](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_set_metadata.png)

Metadata key value pairs can be updated in a similar manner. To remove a metadata key during an update call, supply the `metadata[key]` parameter without setting a value.  This will pass an empty string as part of the request:

![clear metadata key](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_update_metadata.png)

To remove all metadata pass the `metadata` parameter without a value set:

![remove metadata key](https://raw.github.com/dawn-stripe/postman_screenshots/master/postman_remove_metadata.png)






## Changelog
### 2021-06-02
* `Account.company.structure`, `Account#create.company.structure`, `Account#update.company.structure` and `Token#create.account.company.structure` added new enum members: `llc, free_zone_llc, free_zone_establishment and sole_establishment` (breaking change)
* Added support for `documents` on `Person#update`, `Person#create` and `Token#create.person`
* `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]` added new enum members: `identity.verification_session.requires_input, identity.verification_session.redacted, identity.verification_session.processing, identity.verification_session.created, identity.verification_session.canceled and identity.verification_session.verified`
* Added support for `acss_debit` on `PaymentMethod#update`
* `Identity.VerificationReport.created` changed from `integer` to `DateTime` (breaking change)
* `Identity.VerificationSession.client_secret` changed from `string` to `nullable(string)` (breaking change)
* Added support for new resource `Identity.VerificationReport`
* Added support for new resource `Identity.VerificationSession`
* `File#list.purpose` and `File.purpose` added new enum members: `identity_document_downloadable and selfie` (breaking change)
* Removed support for method: `PaymentIntent#verify_microdeposits` (breaking change)
* Removed support for method: `SetupIntent#verify_microdeposits` (breaking change)
* New method: `PaymentIntent#verify_microdeposits`
* New method: `SetupIntent#verify_microdeposits`
* `Account#update.business_profile.support_url` and `Account#create.business_profile.support_url` changed from `string` to `emptyStringable(string)`

### 2021-05-19
* Added support for `reference` on `Charge.payment_method_details.afterpay_clearpay`
* Added support for `afterpay_clearpay` on `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#create.payment_method_options` and `PaymentIntent.payment_method_options`
* `File.purpose` added new enum members: `finance_report_run, document_provider_identity_document and sigma_scheduled_query` (breaking change)
* Added support for `payment_intent` on `EarlyFraudWarning#list` and `Radar.EarlyFraudWarning`
* `SubscriptionItem#create.payment_behavior`, `Subscription#update.payment_behavior`, `Subscription#create.payment_behavior` and `SubscriptionItem#update.payment_behavior` added new enum members: `default_incomplete`
* Added support for `card_present` on `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#create.payment_method_options` and `PaymentIntent.payment_method_options`
* Added support for `currency` on `Checkout.Session.payment_method_options.acss_debit`
* `Account.company.structure`, `Account#create.company.structure`, `Account#update.company.structure` and `Token#create.account.company.structure` added new enum members: `single_member_llc` (breaking change)
* `Issuing.Card.shipping.carrier` added new enum members: `dhl and royal_mail` (breaking change)
* Removed support for the `PaymentPagesCheckoutSessionCheckoutSessionResourcePaymentMethodOptions` resource. (breaking change)
* Added support for `acss_debit_payments` on `Account#create.capabilities`, `Account#update.capabilities` and `Account.capabilities`
* Added support for `acss_debit` on `SetupIntent#confirm.payment_method_options`, `SetupIntent#update.payment_method_options`, `SetupIntent#create.payment_method_options`, `SetupAttempt.payment_method_details`, `PaymentMethod`, `PaymentMethod#create`, `PaymentIntent.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#create.payment_method_data`, `Mandate.payment_method_details`, `Session#create.payment_method_options` and `SetupIntent.payment_method_options`
* Added support for `verify_with_microdeposits` on `PaymentIntent.next_action` and `SetupIntent.next_action`
* `PaymentMethod#list.type`, `PaymentMethod#create.type`, `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `Session#create.payment_method_types[]` and `PaymentMethod.type` added new enum members: `acss_debit` (breaking change)
* `Checkout.Session.payment_method_options` changed from `CheckoutSessionPaymentMethodOptionsForPayment | CheckoutSessionPaymentMethodOptionsForSetup` to `CheckoutSessionPaymentMethodOptionsForPayment` (breaking change)
* Added support for new resource `PaymentPagesCheckoutSessionCheckoutSessionResourcePaymentMethodOptions`
* Added support for `subscription_pause` on `Configuration#update.features`, `Configuration#create.features` and `BillingPortal.Configuration.features`
* Added support for `payment_method_options` on `Session#create` and `Checkout.Session`
* Added support for `transfer_data` on `Session#create.subscription_data`
* Added support for `card_issuing` on `Account#create.settings`, `Account#update.settings` and `Account.settings`
* `Capability.requirements.errors[].code`, `Account.requirements.errors[].code` and `Person.requirements.errors[].code` added new enum members: `verification_missing_owners, verification_missing_executives and verification_requires_additional_memorandum_of_associations` (breaking change)
* `Session#create.locale` and `Checkout.Session.locale` added new enum members: `th` (breaking change)
### 03-17-21:
Initial collection
## We want to hear from you
We want to hear how we can make the collection better! Don't hestiate to file [issues](https://github.com/stripe/stripe-postman/issues) for any bugs you encounters, features you'd like to see or other suggestions you have.
