#CHANGELOG

## Changelog
## 2021-06-02
* API updates
  * Added support for `llc`, `free_zone_llc`, `free_zone_establishment` and `sole_establishment` to the `structure` enum on `Account.company`, `Account#create.company`, `Account#update.company` and `Token#create.account.company.` 
  * Added support for `documents` on `Person#update`, `Person#create` and `Token#create.person`
  * Add support for Identity VerificationSupport and VerificationReport APIs
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

## 2021-05-19
* API updates
  * Added support for `reference` on `Charge.payment_method_details.afterpay_clearpay`
  * Added support for `afterpay_clearpay` on `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#create.payment_method_options` and `PaymentIntent.payment_method_options`
  * `File.purpose` added new enum members: `finance_report_run, document_provider_identity_document and sigma_scheduled_query` (breaking change)
  * Added support for `payment_intent` on `EarlyFraudWarning#list` and `Radar.EarlyFraudWarning`  
  * `SubscriptionItem#create.payment_behavior`, `Subscription#update.payment_behavior`, `Subscription#create.payment_behavior` and `SubscriptionItem#update.payment_behavior` added new enum members: `default_incomplete`
  * Added support for `card_present` on `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#create.payment_method_options` and `PaymentIntent.payment_method_options`
  * `Account.company.structure`, `Account#create.company.structure`, `Account#update.company.structure` and `Token#create.account.company.structure` added new enum members: `single_member_llc` (breaking change)
  * `Issuing.Card.shipping.carrier` added new enum members: `dhl and royal_mail` (breaking change)
  * Removed support for the `PaymentPagesCheckoutSessionCheckoutSessionResourcePaymentMethodOptions` resource. (breaking change)
  * Added support for `currency` on `Checkout.Session.payment_method_options.acss_debit`
  * Added support for `acss_debit_payments` on `Account#create.capabilities`, `Account#update.capabilities` and `Account.capabilities`
  * Added support for `acss_debit` on `SetupIntent#confirm.payment_method_options`, `SetupIntent#update.payment_method_options`, `SetupIntent#create.payment_method_options`, `SetupAttempt.payment_method_details`, `PaymentMethod`, `PaymentMethod#create`, `PaymentIntent.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#create.payment_method_data`, `Mandate.payment_method_details`, `Session#create.payment_method_options` and `SetupIntent.payment_method_options`
  * `PaymentMethod#list.type`, `PaymentMethod#create.type`, `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `Session#create.payment_method_types[]` and `PaymentMethod.type` added new enum members: `acss_debit` (breaking change)
  * `Checkout.Session.payment_method_options` changed from `CheckoutSessionPaymentMethodOptionsForPayment | CheckoutSessionPaymentMethodOptionsForSetup` to `CheckoutSessionPaymentMethodOptionsForPayment` (breaking change)
  * Added support for `verify_with_microdeposits` on `PaymentIntent.next_action` and `SetupIntent.next_action`
  * Added support for new resource `PaymentPagesCheckoutSessionCheckoutSessionResourcePaymentMethodOptions`
  * Added support for `subscription_pause` on `Configuration#update.features`, `Configuration#create.features` and `BillingPortal.Configuration.features`
  * Added support for `payment_method_options` on `Session#create` and `Checkout.Session`
  * Added support for `transfer_data` on `Session#create.subscription_data`
  * Added support for `card_issuing` on `Account#create.settings`, `Account#update.settings` and `Account.settings`
  * `Capability.requirements.errors[].code`, `Account.requirements.errors[].code` and `Person.requirements.errors[].code` added new enum members: `verification_missing_owners, verification_missing_executives and verification_requires_additional_memorandum_of_associations` (breaking change)
  * `Session#create.locale` and `Checkout.Session.locale` added new enum members: `th` (breaking change)
* Collection updates
  * Group resources in shared folders for improved readability
## 03-17-21
Initial collection