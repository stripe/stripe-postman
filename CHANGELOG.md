#CHANGELOG

## Changelog

## 2022-04-06

- Add support for `apply_customer_balance` method on resource `PaymentIntent`
- Add support for `capture_before` on `Charge.payment_method_details.card_present`
- Remove support for `eu_bank_transfer` on `Invoice#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Subscription#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Subscription#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, and `Subscription.payment_settings.payment_method_options.customer_balance.bank_transfer`
- Add support for `request_extended_authorization` on `PaymentIntent#confirm.payment_method_options.card_present`, `PaymentIntent#create.payment_method_options.card_present`, `PaymentIntent#update.payment_method_options.card_present`, and `PaymentIntent.payment_method_options.card_present`
- Add support for `bank_transfer_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
- Add support for `address` and `name` on `Checkout.Session.customer_details`
- Add support for `customer_balance` on `Invoice#create.payment_settings.payment_method_options`, `Invoice#update.payment_settings.payment_method_options`, `Invoice.payment_settings.payment_method_options`, `Subscription#create.payment_settings.payment_method_options`, `Subscription#update.payment_settings.payment_method_options`, and `Subscription.payment_settings.payment_method_options`
- Add support for new value `customer_balance` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
- Add support for new values `payment_intent.partially_funded`, `terminal.reader.action_failed`, and `terminal.reader.action_succeeded` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Change `Charge.failure_balance_transaction`, `Invoice.payment_settings.payment_method_options.us_bank_account`, `PaymentIntent.next_action.verify_with_microdeposits.microdeposit_type`, `SetupIntent.next_action.verify_with_microdeposits.microdeposit_type`, and `Subscription.payment_settings.payment_method_options.us_bank_account` to be required
- Add support for `search` method on resources `Charge`, `Customer`, `Invoice`, `PaymentIntent`, `Price`, `Product`, and `Subscription`
- Add support for `cancel_action`, `process_payment_intent`, `process_setup_intent`, and `set_reader_display` methods on resource `Terminal.Reader`
- Add support for `us_bank_account_ach_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
- Add support for `action` on `Terminal.Reader`
- Add support for `paynow_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
- Add support for `failure_balance_transaction` on `Charge`
- Add support for `paynow` on `Charge.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, and `PaymentMethod`
- Add support for `us_bank_account` on `Charge.payment_method_details`, `Checkout.Session#create.payment_method_options`, `Checkout.Session.payment_method_options`, `Invoice#create.payment_settings.payment_method_options`, `Invoice#update.payment_settings.payment_method_options`, `Invoice.payment_settings.payment_method_options`, `Mandate.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod#update`, `PaymentMethod`, `SetupAttempt.payment_method_details`, `SetupIntent#confirm.payment_method_options`, `SetupIntent#create.payment_method_options`, `SetupIntent#update.payment_method_options`, `SetupIntent.payment_method_options`, `Subscription#create.payment_settings.payment_method_options`, `Subscription#update.payment_settings.payment_method_options`, and `Subscription.payment_settings.payment_method_options`
- Add support for new values `paynow` and `us_bank_account` on enums `Checkout.Session#create.payment_method_types[]` and `PaymentMethod#create.type`
- Add support for new values `paynow` and `us_bank_account` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
- Add support for new values `paynow` and `us_bank_account` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
- Add support for new values `paynow` and `us_bank_account` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, and `PaymentIntent#update.payment_method_data.type`
- Add support for `descriptor_code` on `PaymentIntent#verify_microdeposits` and `SetupIntent#verify_microdeposits`
- Add support for `paynow_display_qr_code` on `PaymentIntent.next_action`
- Add support for `microdeposit_type` on `PaymentIntent.next_action.verify_with_microdeposits` and `SetupIntent.next_action.verify_with_microdeposits`
- Add support for `verification_method` on `PaymentIntentTypeSpecificPaymentMethodOptionsClient` and `SetupIntentTypeSpecificPaymentMethodOptionsClient`
- Add support for new values `paynow` and `us_bank_account` on enum `PaymentMethod.type`
- Add support for `test_clock` on `Subscription#list`
- Add support for new values `bg_uic`, `hu_tin`, and `si_tin` on enums `Checkout.Session.customer_details.tax_ids[].type`, `Invoice.customer_tax_ids[].type`, and `TaxId.type`
- Add support for new values `bg_uic`, `hu_tin`, and `si_tin` on enums `Customer#create.tax_id_data[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, and `TaxId#create.type`
- Add support for `capture_method` on `PaymentIntent#confirm.payment_method_options.afterpay_clearpay`, `PaymentIntent#confirm.payment_method_options.card`, `PaymentIntent#confirm.payment_method_options.klarna`, `PaymentIntent#create.payment_method_options.afterpay_clearpay`, `PaymentIntent#create.payment_method_options.card`, `PaymentIntent#create.payment_method_options.klarna`, `PaymentIntent#update.payment_method_options.afterpay_clearpay`, `PaymentIntent#update.payment_method_options.card`, `PaymentIntent#update.payment_method_options.klarna`, `PaymentIntent.payment_method_options.afterpay_clearpay`, `PaymentIntent.payment_method_options.card`, `PaymentIntent.payment_method_options.klarna`, and `PaymentIntentTypeSpecificPaymentMethodOptionsClient`
- Add support for `test_clock` on `Quote#list`
- Change `Invoice#create.customer` to be optional
- Add support for new values `test_helpers.test_clock.advancing`, `test_helpers.test_clock.created`, `test_helpers.test_clock.deleted`, `test_helpers.test_clock.internal_failure`, and `test_helpers.test_clock.ready` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Add support for `cancel` method on resource `Refund`
- Add support for `status` on `Card`
- Add support for `mandate` on `Charge.payment_method_details.card`
- Add support for `mandate_options` on `PaymentIntent#confirm.payment_method_options.card`, `PaymentIntent#create.payment_method_options.card`, `PaymentIntent#update.payment_method_options.card`, `PaymentIntent.payment_method_options.card`, `SetupIntent#confirm.payment_method_options.card`, `SetupIntent#create.payment_method_options.card`, `SetupIntent#update.payment_method_options.card`, and `SetupIntent.payment_method_options.card`
- Add support for `card_await_notification` on `PaymentIntent.next_action`
- Add support for `customer_notification` on `PaymentIntent.processing.card`
- Change `PaymentLink#create.line_items` to be required
- Add support for `test_clock` on `Customer#list`
- Change `Invoice.test_clock`, `InvoiceItem.test_clock`, `Quote.test_clock`, `Subscription.test_clock`, and `SubscriptionSchedule.test_clock` to be required
- Add support for new resources `CreditedItems` and `ProrationDetails`
- Add support for `proration_details` on `InvoiceLineItem`
- Add support for `next_action` on `Refund`
- Add support for `deletes_after` on `TestHelpers.TestClock`
- Add support for new resource `TestHelpers.TestClock`
- Add support for `test_clock` on `Customer#create`, `Customer`, `InvoiceItem`, `Invoice`, `Quote#create`, `Quote`, `SubscriptionSchedule`, and `Subscription`
- Add support for `pending_invoice_items_behavior` on `Invoice#create`
- Change type of `Product#update.url` from `string` to `emptyStringable(string)`
- Add support for `konbini_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
- Add support for `konbini` on `Charge.payment_method_details`, `Checkout.Session#create.payment_method_options`, `Checkout.Session.payment_method_options`, `Invoice#create.payment_settings.payment_method_options`, `Invoice#update.payment_settings.payment_method_options`, `Invoice.payment_settings.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod`, `Subscription#create.payment_settings.payment_method_options`, `Subscription#update.payment_settings.payment_method_options`, and `Subscription.payment_settings.payment_method_options`
- Add support for new value `konbini` on enums `Checkout.Session#create.payment_method_types[]` and `PaymentMethod#create.type`
- Add support for new value `konbini` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
- Add support for new value `konbini` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
- Add support for new value `konbini` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, and `PaymentIntent#update.payment_method_data.type`
- Add support for `konbini_display_details` on `PaymentIntent.next_action`
- Add support for new value `konbini` on enum `PaymentMethod.type`
- Add support for new resource `SetupIntentTypeSpecificPaymentMethodOptionsClient`
- Change `BillingPortal.Configuration#create.business_profile.privacy_policy_url` and `BillingPortal.Configuration#create.business_profile.terms_of_service_url` to be optional
- Change type of `BillingPortal.Configuration#update.business_profile.privacy_policy_url` and `BillingPortal.Configuration#update.business_profile.terms_of_service_url` from `string` to `emptyStringable(string)`
- Change type of `BillingPortal.Configuration.business_profile.privacy_policy_url` and `BillingPortal.Configuration.business_profile.terms_of_service_url` from `string` to `nullable(string)`
- Add support for `setup_future_usage` on `PaymentIntent#confirm.payment_method_options.acss_debit`, `PaymentIntent#confirm.payment_method_options.afterpay_clearpay`, `PaymentIntent#confirm.payment_method_options.alipay`, `PaymentIntent#confirm.payment_method_options.au_becs_debit`, `PaymentIntent#confirm.payment_method_options.bacs_debit`, `PaymentIntent#confirm.payment_method_options.bancontact`, `PaymentIntent#confirm.payment_method_options.boleto`, `PaymentIntent#confirm.payment_method_options.eps`, `PaymentIntent#confirm.payment_method_options.fpx`, `PaymentIntent#confirm.payment_method_options.giropay`, `PaymentIntent#confirm.payment_method_options.grabpay`, `PaymentIntent#confirm.payment_method_options.ideal`, `PaymentIntent#confirm.payment_method_options.klarna`, `PaymentIntent#confirm.payment_method_options.oxxo`, `PaymentIntent#confirm.payment_method_options.p24`, `PaymentIntent#confirm.payment_method_options.sepa_debit`, `PaymentIntent#confirm.payment_method_options.sofort`, `PaymentIntent#confirm.payment_method_options.wechat_pay`, `PaymentIntent#create.payment_method_options.acss_debit`, `PaymentIntent#create.payment_method_options.afterpay_clearpay`, `PaymentIntent#create.payment_method_options.alipay`, `PaymentIntent#create.payment_method_options.au_becs_debit`, `PaymentIntent#create.payment_method_options.bacs_debit`, `PaymentIntent#create.payment_method_options.bancontact`, `PaymentIntent#create.payment_method_options.boleto`, `PaymentIntent#create.payment_method_options.eps`, `PaymentIntent#create.payment_method_options.fpx`, `PaymentIntent#create.payment_method_options.giropay`, `PaymentIntent#create.payment_method_options.grabpay`, `PaymentIntent#create.payment_method_options.ideal`, `PaymentIntent#create.payment_method_options.klarna`, `PaymentIntent#create.payment_method_options.oxxo`, `PaymentIntent#create.payment_method_options.p24`, `PaymentIntent#create.payment_method_options.sepa_debit`, `PaymentIntent#create.payment_method_options.sofort`, `PaymentIntent#create.payment_method_options.wechat_pay`, `PaymentIntent#update.payment_method_options.acss_debit`, `PaymentIntent#update.payment_method_options.afterpay_clearpay`, `PaymentIntent#update.payment_method_options.alipay`, `PaymentIntent#update.payment_method_options.au_becs_debit`, `PaymentIntent#update.payment_method_options.bacs_debit`, `PaymentIntent#update.payment_method_options.bancontact`, `PaymentIntent#update.payment_method_options.boleto`, `PaymentIntent#update.payment_method_options.eps`, `PaymentIntent#update.payment_method_options.fpx`, `PaymentIntent#update.payment_method_options.giropay`, `PaymentIntent#update.payment_method_options.grabpay`, `PaymentIntent#update.payment_method_options.ideal`, `PaymentIntent#update.payment_method_options.klarna`, `PaymentIntent#update.payment_method_options.oxxo`, `PaymentIntent#update.payment_method_options.p24`, `PaymentIntent#update.payment_method_options.sepa_debit`, `PaymentIntent#update.payment_method_options.sofort`, `PaymentIntent#update.payment_method_options.wechat_pay`, `PaymentIntent.payment_method_options.acss_debit`, `PaymentIntent.payment_method_options.afterpay_clearpay`, `PaymentIntent.payment_method_options.alipay`, `PaymentIntent.payment_method_options.au_becs_debit`, `PaymentIntent.payment_method_options.bacs_debit`, `PaymentIntent.payment_method_options.bancontact`, `PaymentIntent.payment_method_options.boleto`, `PaymentIntent.payment_method_options.eps`, `PaymentIntent.payment_method_options.fpx`, `PaymentIntent.payment_method_options.giropay`, `PaymentIntent.payment_method_options.grabpay`, `PaymentIntent.payment_method_options.ideal`, `PaymentIntent.payment_method_options.klarna`, `PaymentIntent.payment_method_options.oxxo`, `PaymentIntent.payment_method_options.p24`, `PaymentIntent.payment_method_options.sepa_debit`, `PaymentIntent.payment_method_options.sofort`, and `PaymentIntent.payment_method_options.wechat_pay`
- Add support for new values `bbpos_wisepad3` and `stripe_m2` on enums `Terminal.Reader#list.device_type` and `Terminal.Reader.device_type`
- Add support for `verify_microdeposits` method on resources `PaymentIntent` and `SetupIntent`
- Add support for new value `grabpay` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
- Add support for `pin` on `Issuing.Card#update`
- Change type of `Refund.reason` from `string` to `enum('duplicate'|'expired_uncaptured_charge'|'fraudulent'|'requested_by_customer')`

## 2022-01-26

- Add support for new value `au_becs_debit` on enum `Checkout.Session#create.payment_method_types[]`
- Add support for new value `is_vat` on enums `Checkout.Session.customer_details.tax_ids[].type`, `Invoice.customer_tax_ids[].type`, and `TaxId.type`
- Change `Checkout.Session.payment_link` to be required
- Add support for new value `is_vat` on enums `Customer#create.tax_id_data[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, and `TaxId#create.type`
- Add support for `phone_number_collection` on `PaymentLink#create` and `PaymentLink`
- Add support for new values `payment_link.created` and `payment_link.updated` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Add support for new resource `PaymentLink`
- Add support for `payment_link` on `Checkout.Session`
- Add support for `image_url_png` and `image_url_svg` on `PaymentIntent.next_action.wechat_pay_display_qr_code`
- Change type of `Charge.status` from `string` to `enum('failed'|'pending'|'succeeded')`
- Add support for `bacs_debit` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Add support for `eps` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Add support for `customer_creation` on `Checkout.Session#create` and `Checkout.Session`
- Add support for `paid_out_of_band` on `Invoice`
- Add support for `fpx` and `grabpay` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Add support for `mandate_options` on `Subscription#create.payment_settings.payment_method_options.card`, `Subscription#update.payment_settings.payment_method_options.card`, and `Subscription.payment_settings.payment_method_options.card`
- Change type of `PaymentIntent.processing.type` from `string` to `literal('card')`
- Add support for `au_becs_debit` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Add support for new values `en-FR`, `es-US`, and `fr-FR` on enums `PaymentIntent#create.payment_method_options.klarna.preferred_locale`, `PaymentIntent#update.payment_method_options.klarna.preferred_locale`, and `PaymentIntent#confirm.payment_method_options.klarna.preferred_locale`
- Add support for `boleto` on `SetupAttempt.payment_method_details`
- Add support for `processing` on `PaymentIntent`

### 2021-12-15

- Add support for new resource `PaymentIntentTypeSpecificPaymentMethodOptionsClient`
- Add support for `setup_future_usage` on `PaymentIntent#create.payment_method_options.card`, `PaymentIntent#update.payment_method_options.card`, `PaymentIntent#confirm.payment_method_options.card`, and `PaymentIntent.payment_method_options.card`
- Add support for `metadata` on `BillingPortal.Configuration#create`, `BillingPortal.Configuration#update`, and `BillingPortal.Configuration`
- Add support for new values `ge_vat` and `ua_vat` on enums `Checkout.Session.customer_details.tax_ids[].type`, `Invoice.customer_tax_ids[].type`, and `TaxId.type`
- Add support for new values `ge_vat` and `ua_vat` on enums `Customer#create.tax_id_data[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, and `TaxId#create.type`
- Add support for new value `en-IE` on enums `PaymentIntent#create.payment_method_options.klarna.preferred_locale`, `PaymentIntent#update.payment_method_options.klarna.preferred_locale`, and `PaymentIntent#confirm.payment_method_options.klarna.preferred_locale`
- Change type of `PaymentIntent#create.payment_method_data.billing_details.email`, `PaymentIntent#update.payment_method_data.billing_details.email`, `PaymentIntent#confirm.payment_method_data.billing_details.email`, `PaymentMethod#create.billing_details.email`, and `PaymentMethod#update.billing_details.email` from `string` to `emptyStringable(string)`
- Add support for `giropay` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Add support for `wallets` on `Issuing.Card`
- Add support for new value `jct` on enums `TaxRate#create.tax_type`, `TaxRate#update.tax_type`, and `TaxRate.tax_type`
- Add support for new resource `AutomaticPaymentMethodsPaymentIntent`
- Add support for `automatic_payment_methods` on `PaymentIntent#create` and `PaymentIntent`
- Add support for new resource `ShippingRate`
- Add support for `shipping_options` on `Checkout.Session#create` and `Checkout.Session`
- Add support for `shipping_rate` on `Checkout.Session`
- Add support for `interac_present` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Add support for new value `agrobank` on enums `Charge.payment_method_details.fpx.bank`, `PaymentIntent#create.payment_method_data.fpx.bank`, `PaymentIntent#update.payment_method_data.fpx.bank`, `PaymentIntent#confirm.payment_method_data.fpx.bank`, `PaymentMethod#create.fpx.bank`, and `PaymentMethod.fpx.bank`
- Add support for `expire` method on resource `Checkout.Session`
- Add support for `status` on `Checkout.Session`
- Remove support for `ownership_declaration_shown_and_signed` on `Token#create.account`
- Add support for `ownership_declaration_shown_and_signed` on `Token#create.account.company`

### 2021-11-01

- Add support for `ownership_declaration` on `Account#update.company`, `Account#create.company`, `Account.company`, and `Token#create.account.company`
- Add support for `proof_of_registration` on `Account#update.documents` and `Account#create.documents`
- Change type of `Account#update.individual.full_name_aliases`, `Account#create.individual.full_name_aliases`, `Person#create.full_name_aliases`, `Person#update.full_name_aliases`, `Token#create.account.individual.full_name_aliases`, and `Token#create.person.full_name_aliases` from `array(string)` to `emptyStringable(array(string))`
- Add support for `ownership_declaration_shown_and_signed` on `Token#create.account`
- Add support for new values `en-BE`, `en-ES`, and `en-IT` on enums `PaymentIntent#create.payment_method_options.klarna.preferred_locale`, `PaymentIntent#update.payment_method_options.klarna.preferred_locale`, and `PaymentIntent#confirm.payment_method_options.klarna.preferred_locale`
- Add support for `buyer_id` on `Charge.payment_method_details.alipay`
- Change `Account.controller.type` to be required
- Change type of `UsageRecord#create.timestamp` from `integer` to `literal('now') | integer`
- Change `UsageRecord#create.timestamp` to be optional
- Change `Checkout.Session.customer_details.phone` to be required
- Add support for new value `klarna` on enum `Checkout.Session#create.payment_method_types[]`
- Change `Checkout.Session.customer_details.phone` to be optional
- Change `Charge.payment_method_details.klarna.payment_method_category`, `Charge.payment_method_details.klarna.preferred_locale`, `Checkout.Session.customer_details.phone`, and `PaymentMethod.klarna.dob` to be required
- Add support for `list_payment_methods` method on resource `Customer`
- Add support for `payment_method_category` and `preferred_locale` on `Charge.payment_method_details.klarna`
- Add support for `klarna` on `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, and `PaymentMethod`
- Add support for new value `klarna` on enums `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, and `PaymentIntent#confirm.payment_method_data.type`
- Add support for new value `klarna` on enum `PaymentMethod#create.type`
- Add support for new value `klarna` on enum `PaymentMethod#list.type`
- Add support for new value `klarna` on enum `PaymentMethod.type`
- Add support for `phone_number_collection` on `Checkout.Session#create` and `Checkout.Session`
- Add support for `phone` on `Checkout.Session.customer_details`
- Add support for new value `customer_id` on enums `Radar.ValueList#create.item_type` and `Radar.ValueList.item_type`
- Add support for new value `bbpos_wisepos_e` on enums `Terminal.Reader#list.device_type` and `Terminal.Reader.device_type`
- Change `PaymentMethod#list.customer` to be optional
- Add support for `klarna_payments` on `Account#update.capabilities`, `Account#create.capabilities`, and `Account.capabilities`

### 2021-09-20

- Add support for `amount_authorized` and `overcapture_supported` on `Charge.payment_method_details.card_present`
- Add support for `full_name_aliases` on `Account#update.individual`, `Account#create.individual`, `Person#create`, `Person#update`, `Person`, `Token#create.account.individual`, and `Token#create.person`
- Change `BillingPortal.Configuration.features.subscription_cancel.cancellation_reason` to be required
- Add support for `default_for` on `Checkout.Session#create.payment_method_options.acss_debit.mandate_options`, `Checkout.Session.payment_method_options.acss_debit.mandate_options`, `Mandate.payment_method_details.acss_debit`, `SetupIntent#create.payment_method_options.acss_debit.mandate_options`, `SetupIntent#update.payment_method_options.acss_debit.mandate_options`, `SetupIntent#confirm.payment_method_options.acss_debit.mandate_options`, and `SetupIntent.payment_method_options.acss_debit.mandate_options`
- Add support for `acss_debit` on `Invoice#create.payment_settings.payment_method_options`, `Invoice#update.payment_settings.payment_method_options`, `Invoice.payment_settings.payment_method_options`, `Subscription#create.payment_settings.payment_method_options`, `Subscription#update.payment_settings.payment_method_options`, and `Subscription.payment_settings.payment_method_options`
- Add support for new value `acss_debit` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
- Add support for `livemode` on `Reporting.ReportType`
- Add support for new value `rst` on enums `TaxRate#create.tax_type`, `TaxRate#update.tax_type`, and `TaxRate.tax_type`
- Change `Checkout.Session.after_expiration`, `Checkout.Session.consent`, `Checkout.Session.consent_collection`, `Checkout.Session.expires_at`, and `Checkout.Session.recovered_from` to be required
- Add support for new value `checkout.session.expired` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Change `Account.future_requirements.alternatives`, `Account.requirements.alternatives`, `Capability.future_requirements.alternatives`, `Capability.requirements.alternatives`, `Person.future_requirements.alternatives`, and `Person.requirements.alternatives` to be required
- Change type of `Capability.future_requirements.alternatives`, `Capability.requirements.alternatives`, `Person.future_requirements.alternatives`, and `Person.requirements.alternatives` from `array(AccountRequirementsAlternative)` to `nullable(array(AccountRequirementsAlternative))`
- Add support for `future_requirements` on `Account`, `Capability`, and `Person`
- Add support for `alternatives` on `Account.requirements`, `Capability.requirements`, and `Person.requirements`
- Change type of `Checkout.Session.after_expiration.recovery.allow_promotion_codes` and `Checkout.Session.after_expiration.recovery.enabled` from `nullable(boolean)` to `boolean`
- Add support for `after_expiration`, `consent_collection`, and `expires_at` on `Checkout.Session#create` and `Checkout.Session`
- Add support for `consent` and `recovered_from` on `Checkout.Session`
- Change type of `BillingPortal.Configuration#create.features.subscription_cancel.cancellation_reason.options[]`, `BillingPortal.Configuration#update.features.subscription_cancel.cancellation_reason.options[]`, and `BillingPortal.Configuration.features.subscription_cancel.cancellation_reason.options[]` from `string` to `enum`
- Add support for `cancellation_reason` on `BillingPortal.Configuration.features.subscription_cancel`
- Add support for `cancellation_reason` on `BillingPortal.Configuration#create.features.subscription_cancel` and `BillingPortal.Configuration#update.features.subscription_cancel`

### 2021-08-24

- Add support for `category_code` on `Issuing.Authorization.merchant_data` and `Issuing.Transaction.merchant_data`
- Add support for new value `redacted` on enum `Review.closed_reason`
- Add support for new values `hr`, `ko`, and `vi` on enums `Checkout.Session#create.locale` and `Checkout.Session.locale`

### 2021-07-20

- Add support for `ideal` on `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, and `PaymentIntent.payment_method_options`
- Remove support for values `api_connection_error`, `authentication_error`, and `rate_limit_error` from enums `StripeError.type`, `StripeErrorResponse.error.type`, `Invoice.last_finalization_error.type`, `PaymentIntent.last_payment_error.type`, `SetupAttempt.setup_error.type`, and `SetupIntent.last_setup_error.type`
- Add support for new values `quote.accepted`, `quote.canceled`, `quote.created`, and `quote.finalized` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Add support for `list_computed_upfront_line_items` method on resource `Quote`
- Add support for `finalize_quote` method on resource `Quote`
- Remove support for `finalize` method on resource `Quote`
- Add support for new resource `Quote`
- Add support for `quote` on `Invoice`
- Add support for new value `quote_accept` on enum `Invoice.billing_reason`
- Changed type of `Charge.payment_method_details.card.three_d_secure.result` and `SetupAttempt.payment_method_details.card.three_d_secure.result` from `enum` to `nullable(enum)`
- Changed type of `Charge.payment_method_details.card.three_d_secure.version` and `SetupAttempt.payment_method_details.card.three_d_secure.version` from `enum('1.0.2'|'2.1.0'|'2.2.0')` to `nullable(enum('1.0.2'|'2.1.0'|'2.2.0'))`
- Add support for new value `boleto` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, and `Invoice.payment_settings.payment_method_types[]`
- Add support for `boleto_payments` on `Account#update.capabilities`, `Account#create.capabilities`, and `Account.capabilities`
- Add support for `wechat_pay` on `Charge.payment_method_details`, `Checkout.Session#create.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, and `PaymentMethod`
- Add support for `boleto` and `oxxo` on `Checkout.Session#create.payment_method_options` and `Checkout.Session.payment_method_options`
- Add support for new values `boleto`, `oxxo`, and `wechat_pay` on enum `Checkout.Session#create.payment_method_types[]`
- Add support for new value `wechat_pay` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, and `Invoice.payment_settings.payment_method_types[]`
- Add support for new value `wechat_pay` on enums `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, and `PaymentIntent#confirm.payment_method_data.type`
- Add support for `wechat_pay_display_qr_code`, `wechat_pay_redirect_to_android_app`, and `wechat_pay_redirect_to_ios_app` on `PaymentIntent.next_action`
- Add support for new value `wechat_pay` on enum `PaymentMethod#create.type`
- Add support for new value `wechat_pay` on enum `PaymentMethod#list.type`
- Add support for new value `wechat_pay` on enum `PaymentMethod.type`
- Add support for `boleto` on `Charge.payment_method_details`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, and `PaymentMethod`
- Add support for new value `boleto` on enums `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, and `PaymentIntent#confirm.payment_method_data.type`
- Add support for `boleto_display_details` on `PaymentIntent.next_action`
- Add support for new value `boleto` on enum `PaymentMethod#create.type`
- Add support for new value `boleto` on enum `PaymentMethod#list.type`
- Add support for new value `boleto` on enum `PaymentMethod.type`
- Collection updates:
  - Fixed issue where nested dictionary child parameters weren't being populated

### 2021-06-22

- API updates
  - `TaxId#create.type`, `Invoice.customer_tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Customer#create.tax_id_data[].type`, `Checkout.Session.customer_details.tax_ids[].type` and `TaxId.type` added new enum members: `il_vat` (breaking change)
  - `TaxId#create.type`, `Invoice.customer_tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Customer#create.tax_id_data[].type`, `Checkout.Session.customer_details.tax_ids[].type` and `TaxId.type` added new enum members: `ca_pst_mb, ca_pst_bc, ca_gst_hst and ca_pst_sk` (breaking change)
  - Added support for `url` on `Checkout.Session`
  - Added support for `tax_id_collection` on `Session#create` and `Checkout.Session`
  - `Terminal.Reader.location` changed from `string` to `expandable($Terminal.Location)` (breaking change)
  - Added support for `controller` on `Account`
  - Added support for new resource `TaxCode`
  - Added support for `automatic_tax` on `SubscriptionSchedule.default_settings`, `SubscriptionSchedule#update.phases[]`, `SubscriptionSchedule#update.default_settings`, `SubscriptionSchedule#create.phases[]`, `SubscriptionSchedule#create.default_settings`, `Subscription`, `Subscription#update`, `Subscription#create`, `Invoice`, `Invoice#upcomingLines`, `Invoice#update`, `Invoice#upcoming`, `Invoice#create`, `Checkout.Session`, `Session#create` and `SubscriptionSchedule.phases[]`
  - Added support for `customer_update` on `Session#create`
  - Added support for `tax_behavior` on `SubscriptionSchedule#update.phases[].add_invoice_items[].price_data`, `SubscriptionSchedule#create.phases[].items[].price_data`, `SubscriptionSchedule#create.phases[].add_invoice_items[].price_data`, `SubscriptionItem#update.price_data`, `SubscriptionItem#create.price_data`, `Subscription#update.items[].price_data`, `Subscription#update.add_invoice_items[].price_data`, `Subscription#create.items[].price_data`, `Subscription#create.add_invoice_items[].price_data`, `Price`, `Price#update`, `Price#create`, `InvoiceItem#update.price_data`, `InvoiceItem#create.price_data`, `Invoice#upcomingLines.subscription_items[].price_data`, `Invoice#upcomingLines.invoice_items[].price_data`, `Invoice#upcoming.subscription_items[].price_data`, `Invoice#upcoming.invoice_items[].price_data`, `Session#create.line_items[].price_data` and `SubscriptionSchedule#update.phases[].items[].price_data`
  - Added support for `tax_code` on `Product#update`, `Product#create`, `Price#create.product_data`, `Plan#create.product[0]`, `Session#create.line_items[].price_data.product_data` and `Product`
  - Added support for `tax` on `Customer#update`, `Customer#create` and `Customer`
  - Added support for `customer_details` on `Invoice#upcoming` and `Invoice#upcomingLines`
  - Added support for `tax_type` on `TaxRate#update`, `TaxRate#create` and `TaxRate`
- Collection updates:
  - Fixed issue where some required parameters weren't being selected by default in the request
  - Fixed typos in request names

### 2021-06-02

- API updates
  - Added support for `llc`, `free_zone_llc`, `free_zone_establishment` and `sole_establishment` to the `structure` enum on `Account.company`, `Account#create.company`, `Account#update.company` and `Token#create.account.company.`
  - Added support for `documents` on `Person#update`, `Person#create` and `Token#create.person`
  - Add support for Identity VerificationSupport and VerificationReport APIs
  - Added support for `acss_debit` on `PaymentMethod#update`
  - `Identity.VerificationReport.created` changed from `integer` to `DateTime` (breaking change)
  - `Identity.VerificationSession.client_secret` changed from `string` to `nullable(string)` (breaking change)
  - Added support for new resource `Identity.VerificationReport`
  - Added support for new resource `Identity.VerificationSession`
  - `File#list.purpose` and `File.purpose` added new enum members: `identity_document_downloadable and selfie` (breaking change)
  - Removed support for method: `PaymentIntent#verify_microdeposits` (breaking change)
  - Removed support for method: `SetupIntent#verify_microdeposits` (breaking change)
  - New method: `PaymentIntent#verify_microdeposits`
  - New method: `SetupIntent#verify_microdeposits`

### 2021-05-19

- API updates
  - Added support for `reference` on `Charge.payment_method_details.afterpay_clearpay`
  - Added support for `afterpay_clearpay` on `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#create.payment_method_options` and `PaymentIntent.payment_method_options`
  - `File.purpose` added new enum members: `finance_report_run, document_provider_identity_document and sigma_scheduled_query` (breaking change)
  - Added support for `payment_intent` on `EarlyFraudWarning#list` and `Radar.EarlyFraudWarning`
  - `SubscriptionItem#create.payment_behavior`, `Subscription#update.payment_behavior`, `Subscription#create.payment_behavior` and `SubscriptionItem#update.payment_behavior` added new enum members: `default_incomplete`
  - Added support for `card_present` on `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#create.payment_method_options` and `PaymentIntent.payment_method_options`
  - `Account.company.structure`, `Account#create.company.structure`, `Account#update.company.structure` and `Token#create.account.company.structure` added new enum members: `single_member_llc` (breaking change)
  - `Issuing.Card.shipping.carrier` added new enum members: `dhl and royal_mail` (breaking change)
  - Removed support for the `PaymentPagesCheckoutSessionCheckoutSessionResourcePaymentMethodOptions` resource. (breaking change)
  - Added support for `currency` on `Checkout.Session.payment_method_options.acss_debit`
  - Added support for `acss_debit_payments` on `Account#create.capabilities`, `Account#update.capabilities` and `Account.capabilities`
  - Added support for `acss_debit` on `SetupIntent#confirm.payment_method_options`, `SetupIntent#update.payment_method_options`, `SetupIntent#create.payment_method_options`, `SetupAttempt.payment_method_details`, `PaymentMethod`, `PaymentMethod#create`, `PaymentIntent.payment_method_options`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#create.payment_method_data`, `Mandate.payment_method_details`, `Session#create.payment_method_options` and `SetupIntent.payment_method_options`
  - `PaymentMethod#list.type`, `PaymentMethod#create.type`, `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `Session#create.payment_method_types[]` and `PaymentMethod.type` added new enum members: `acss_debit` (breaking change)
  - `Checkout.Session.payment_method_options` changed from `CheckoutSessionPaymentMethodOptionsForPayment | CheckoutSessionPaymentMethodOptionsForSetup` to `CheckoutSessionPaymentMethodOptionsForPayment` (breaking change)
  - Added support for `verify_with_microdeposits` on `PaymentIntent.next_action` and `SetupIntent.next_action`
  - Added support for new resource `PaymentPagesCheckoutSessionCheckoutSessionResourcePaymentMethodOptions`
  - Added support for `subscription_pause` on `Configuration#update.features`, `Configuration#create.features` and `BillingPortal.Configuration.features`
  - Added support for `payment_method_options` on `Session#create` and `Checkout.Session`
  - Added support for `transfer_data` on `Session#create.subscription_data`
  - Added support for `card_issuing` on `Account#create.settings`, `Account#update.settings` and `Account.settings`
  - `Capability.requirements.errors[].code`, `Account.requirements.errors[].code` and `Person.requirements.errors[].code` added new enum members: `verification_missing_owners, verification_missing_executives and verification_requires_additional_memorandum_of_associations` (breaking change)
  - `Session#create.locale` and `Checkout.Session.locale` added new enum members: `th` (breaking change)
- Collection updates
  - Group resources in shared folders for improved readability

### 03-17-21

Initial collection
