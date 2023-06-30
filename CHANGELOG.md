#CHANGELOG

## Changelog

## 2023-06-22
* Add support for `on_behalf_of` on `Mandate`
* Change type of `Checkout.Session.success_url` from `string` to `nullable(string)`
* Change type of `File#create.file` from `string` to `file`
* Add support for `taxability_reason` on `Tax.Calculation.tax_breakdown[]`
* Change `Charge.payment_method_details.cashapp.buyer_id`, `Charge.payment_method_details.cashapp.cashtag`, `PaymentMethod.cashapp.buyer_id`, and `PaymentMethod.cashapp.cashtag` to be required
* Add support for `numeric` and `text` on `Checkout.Session#create.custom_fields[]`, `PaymentLink#create.custom_fields[]`, and `PaymentLink#update.custom_fields[]`
* Add support for new values `aba` and `swift` on enums `Checkout.Session#create.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Checkout.Session.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`
* Add support for new value `us_bank_transfer` on enums `Checkout.Session#create.payment_method_options.customer_balance.bank_transfer.type`, `Checkout.Session.payment_method_options.customer_balance.bank_transfer.type`, `Customer#create_funding_instructions.bank_transfer.type`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent.next_action.display_bank_transfer_instructions.type`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.type`
* Add support for `maximum_length` and `minimum_length` on `Checkout.Session.custom_fields[].numeric` and `Checkout.Session.custom_fields[].text`
* Add support for `payer_email` on `PaymentMethod.paypal`
* Add support for `preferred_locales` on `Issuing.Cardholder#create`, `Issuing.Cardholder#update`, and `Issuing.Cardholder`
* Add support for `description`, `iin`, and `issuer` on `PaymentMethod.card_present` and `PaymentMethod.interac_present`
* Add support for `zip_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
* Add support for `zip` on `Charge.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod#update`, `PaymentMethod`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#create.payment_method_data`, and `SetupIntent#update.payment_method_data`
* Add support for new value `zip` on enums `Checkout.Session#create.payment_method_types[]` and `PaymentMethod#create.type`
* Add support for new value `zip` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
* Add support for new value `zip` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `SetupIntent#confirm.payment_method_data.type`, `SetupIntent#create.payment_method_data.type`, and `SetupIntent#update.payment_method_data.type`
* Add support for new value `zip` on enum `PaymentMethod.type`
* Change type of `Invoice.last_finalization_error.code`, `PaymentIntent.last_payment_error.code`, `SetupAttempt.setup_error.code`, `SetupIntent.last_setup_error.code`, and `StripeError.code` from `string` to `enum`
* Add support for new values `amusement_tax` and `communications_tax` on enums `TaxRate#create.tax_type`, `TaxRate#update.tax_type`, and `TaxRate.tax_type`

* Add support for `subscription_update_confirm` and `subscription_update` on `BillingPortal.Session#create.flow_data` and `BillingPortal.Session.flow`
* Add support for new values `subscription_update_confirm` and `subscription_update` on enums `BillingPortal.Session#create.flow_data.type` and `BillingPortal.Session.flow.type`
* Add support for `link` on `Charge.payment_method_details.card.wallet` and `PaymentMethod.card.wallet`

* Add support for `buyer_id` and `cashtag` on `Charge.payment_method_details.cashapp` and `PaymentMethod.cashapp`

* Add support for `taxability_reason` and `taxable_amount` on `Checkout.Session.shipping_cost.taxes[]`, `Checkout.Session.total_details.breakdown.taxes[]`, `CreditNote.shipping_cost.taxes[]`, `CreditNote.tax_amounts[]`, `Invoice.shipping_cost.taxes[]`, `Invoice.total_tax_amounts[]`, `LineItem.taxes[]`, `Quote.computed.recurring.total_details.breakdown.taxes[]`, `Quote.computed.upfront.total_details.breakdown.taxes[]`, and `Quote.total_details.breakdown.taxes[]`
* Add support for `effective_percentage` on `TaxRate`

* Add support for `network_token` on `Charge.payment_method_details.card`
* Add support for `brand`, `cardholder_name`, `country`, `exp_month`, `exp_year`, `fingerprint`, `funding`, `last4`, `networks`, and `read_method` on `PaymentMethod.card_present` and `PaymentMethod.interac_present`
* Add support for `preferred_locales` on `PaymentMethod.interac_present`

* Add support for `paypal` on `Charge.payment_method_details`, `Checkout.Session#create.payment_method_options`, `Mandate.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod`, `SetupAttempt.payment_method_details`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#confirm.payment_method_options`, `SetupIntent#create.payment_method_data`, `SetupIntent#create.payment_method_options`, `SetupIntent#update.payment_method_data`, `SetupIntent#update.payment_method_options`, and `SetupIntent.payment_method_options`
* Add support for new value `paypal` on enums `Checkout.Session#create.payment_method_types[]` and `PaymentMethod#create.type`
* Add support for new value `paypal` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
* Add support for new value `paypal` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
* Add support for new value `paypal` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `SetupIntent#confirm.payment_method_data.type`, `SetupIntent#create.payment_method_data.type`, and `SetupIntent#update.payment_method_data.type`
* Add support for new value `paypal` on enums `PaymentLink#create.payment_method_types[]`, `PaymentLink#update.payment_method_types[]`, and `PaymentLink.payment_method_types[]`
* Add support for new value `paypal` on enum `PaymentMethod.type`

* Add support for new value `eftpos_au` on enums `PaymentIntent#confirm.payment_method_options.card.network`, `PaymentIntent#create.payment_method_options.card.network`, `PaymentIntent#update.payment_method_options.card.network`, `PaymentIntent.payment_method_options.card.network`, `SetupIntent#confirm.payment_method_options.card.network`, `SetupIntent#create.payment_method_options.card.network`, `SetupIntent#update.payment_method_options.card.network`, `SetupIntent.payment_method_options.card.network`, `Subscription#create.payment_settings.payment_method_options.card.network`, `Subscription#update.payment_settings.payment_method_options.card.network`, and `Subscription.payment_settings.payment_method_options.card.network`

* Add support for `link` on `Checkout.Session#create.payment_method_options` and `Checkout.Session.payment_method_options`

* Add support for `brand`, `country`, `description`, `exp_month`, `exp_year`, `fingerprint`, `funding`, `iin`, `issuer`, `last4`, `network`, and `wallet` on `SetupAttempt.payment_method_details.card`

* Add support for `tax_breakdown` on `Tax.Calculation.shipping_cost` and `Tax.Transaction.shipping_cost`

* Add support for `billing_cycle_anchor` and `proration_behavior` on `Checkout.Session#create.subscription_data`

* Add support for `terminal_id` on `Issuing.Authorization.merchant_data` and `Issuing.Transaction.merchant_data`

* Add support for `checks` on `SetupAttempt.payment_method_details.card`

* Add support for `metadata` on `PaymentIntent#capture`

* Change `Identity.VerificationReport.options` and `Identity.VerificationReport.type` to be optional
* Change type of `Identity.VerificationSession.options` from `GelatoVerificationSessionOptions` to `nullable(GelatoVerificationSessionOptions)`
* Change type of `Identity.VerificationSession.type` from `enum('document'|'id_number')` to `nullable(enum('document'|'id_number'))`

* Add support for new value `REVOIE23` on enums `Charge.payment_method_details.ideal.bic`, `PaymentMethod.ideal.bic`, and `SetupAttempt.payment_method_details.ideal.bic`
* Change `Checkout.Session.currency_conversion` to be required

* Add support for new value `link` on enums `Charge.payment_method_details.card.wallet.type` and `PaymentMethod.card.wallet.type`
* Change `Issuing.Cardholder#create.type` to be optional
* Add support for `status_details` on `PaymentMethod.us_bank_account`

* Add support for `country` on `PaymentMethod.link`

* Remove support for `create` method on resource `Tax.Transaction`
* Add support for `export_license_id` and `export_purpose_code` on `Account#create.company`, `Account#update.company`, `Account.company`, and `Token#create.account.company`

* Add support for `amount_tip` on `Terminal.Reader.testHelpers#present_payment_method`

* Remove support for value `deleted` from enum `Invoice.status`

* Add support for new resources `Tax.CalculationLineItem`, `Tax.Calculation`, `Tax.TransactionLineItem`, and `Tax.Transaction`
* Add support for `create` and `list_line_items` methods on resource `Calculation`
* Add support for `create_from_calculation`, `create_reversal`, `create`, `list_line_items`, and `retrieve` methods on resource `Transaction`

* Add support for `currency_conversion` on `Checkout.Session`

* Add support for new value `link` on enums `PaymentLink#create.payment_method_types[]`, `PaymentLink#update.payment_method_types[]`, and `PaymentLink.payment_method_types[]`

* Add support for new value `link` on enum `Checkout.Session#create.payment_method_types[]`
* Add support for `automatic_payment_methods` on `SetupIntent#create` and `SetupIntent`

* Add support for `future_requirements` and `requirements` on `BankAccount`
* Add support for `country` on `Charge.payment_method_details.link`
* Add support for new value `automatic_async` on enums `Checkout.Session#create.payment_intent_data.capture_method`, `PaymentIntent#confirm.capture_method`, `PaymentIntent#create.capture_method`, `PaymentIntent#update.capture_method`, `PaymentIntent.capture_method`, `PaymentLink#create.payment_intent_data.capture_method`, and `PaymentLink.payment_intent_data.capture_method`

* Add support for `preferred_locale` on `PaymentIntent#confirm.payment_method_options.affirm`, `PaymentIntent#create.payment_method_options.affirm`, `PaymentIntent#update.payment_method_options.affirm`, and `PaymentIntent.payment_method_options.affirm`

* Add support for `cashapp_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
* Add support for `cashapp` on `Charge.payment_method_details`, `Mandate.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod#update`, `PaymentMethod`, `SetupAttempt.payment_method_details`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#create.payment_method_data`, and `SetupIntent#update.payment_method_data`
* Add support for new value `cashapp` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
* Add support for new value `cashapp` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
* Add support for new value `cashapp` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `SetupIntent#confirm.payment_method_data.type`, `SetupIntent#create.payment_method_data.type`, and `SetupIntent#update.payment_method_data.type`
* Add support for `cashapp_handle_redirect_or_display_qr_code` on `PaymentIntent.next_action` and `SetupIntent.next_action`
* Add support for new value `cashapp` on enum `PaymentMethod#create.type`
* Add support for new value `cashapp` on enum `PaymentMethod.type`

* Add support for `cashapp` on `Checkout.Session#create.payment_method_options` and `Checkout.Session.payment_method_options`
* Add support for new value `cashapp` on enum `Checkout.Session#create.payment_method_types[]`
* Add support for new value `cashapp` on enums `PaymentLink#create.payment_method_types[]`, `PaymentLink#update.payment_method_types[]`, and `PaymentLink.payment_method_types[]`

* Add support for new value `payout.reconciliation_completed` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`

* Add support for `card_issuing` on `Issuing.Cardholder#create.individual` and `Issuing.Cardholder#update.individual`
* Add support for new value `requirements.past_due` on enum `Issuing.Cardholder.requirements.disabled_reason`
* Add support for new values `individual.card_issuing.user_terms_acceptance.date` and `individual.card_issuing.user_terms_acceptance.ip` on enum `Issuing.Cardholder.requirements.past_due[]`

* Add support for `cancellation_details` on `Subscription#cancel`, `Subscription#update`, and `Subscription`

* Add support for `reconciliation_status` on `Payout`
* Add support for new value `lease_tax` on enums `TaxRate#create.tax_type`, `TaxRate#update.tax_type`, and `TaxRate.tax_type`

* Add support for new values `electric_vehicle_charging`, `emergency_services_gcas_visa_use_only`, `government_licensed_horse_dog_racing_us_region_only`, `government_licensed_online_casions_online_gambling_us_region_only`, `government_owned_lotteries_non_us_region`, `government_owned_lotteries_us_region_only`, and `marketplaces` on enums `Issuing.Card#create.spending_controls.allowed_categories[]`, `Issuing.Card#create.spending_controls.blocked_categories[]`, `Issuing.Card#create.spending_controls.spending_limits[].categories[]`, `Issuing.Card#update.spending_controls.allowed_categories[]`, `Issuing.Card#update.spending_controls.blocked_categories[]`, `Issuing.Card#update.spending_controls.spending_limits[].categories[]`, `Issuing.Card.spending_controls.allowed_categories[]`, `Issuing.Card.spending_controls.blocked_categories[]`, `Issuing.Card.spending_controls.spending_limits[].categories[]`, `Issuing.Cardholder#create.spending_controls.allowed_categories[]`, `Issuing.Cardholder#create.spending_controls.blocked_categories[]`, `Issuing.Cardholder#create.spending_controls.spending_limits[].categories[]`, `Issuing.Cardholder#update.spending_controls.allowed_categories[]`, `Issuing.Cardholder#update.spending_controls.blocked_categories[]`, `Issuing.Cardholder#update.spending_controls.spending_limits[].categories[]`, `Issuing.Cardholder.spending_controls.allowed_categories[]`, `Issuing.Cardholder.spending_controls.blocked_categories[]`, and `Issuing.Cardholder.spending_controls.spending_limits[].categories[]`

* Add support for new value `igst` on enums `TaxRate#create.tax_type`, `TaxRate#update.tax_type`, and `TaxRate.tax_type`

* Add support for new value `yoursafe` on enums `Charge.payment_method_details.ideal.bank`, `PaymentIntent#confirm.payment_method_data.ideal.bank`, `PaymentIntent#create.payment_method_data.ideal.bank`, `PaymentIntent#update.payment_method_data.ideal.bank`, `PaymentMethod#create.ideal.bank`, `PaymentMethod.ideal.bank`, `SetupAttempt.payment_method_details.ideal.bank`, `SetupIntent#confirm.payment_method_data.ideal.bank`, `SetupIntent#create.payment_method_data.ideal.bank`, and `SetupIntent#update.payment_method_data.ideal.bank`
* Add support for new value `BITSNL2A` on enums `Charge.payment_method_details.ideal.bic`, `PaymentMethod.ideal.bic`, and `SetupAttempt.payment_method_details.ideal.bic`

* Add support for `refund_payment` method on resource `Terminal.Reader`
* Add support for new value `name` on enums `BillingPortal.Configuration#create.features.customer_update.allowed_updates[]`, `BillingPortal.Configuration#update.features.customer_update.allowed_updates[]`, and `BillingPortal.Configuration.features.customer_update.allowed_updates[]`
* Add support for `custom_fields` on `Checkout.Session#create`, `Checkout.Session`, `PaymentLink#create`, `PaymentLink#update`, and `PaymentLink`
* Add support for `interac_present` on `Terminal.Reader.testHelpers#present_payment_method`
* Change type of `Terminal.Reader.testHelpers#present_payment_method.type` from `literal('card_present')` to `enum('card_present'|'interac_present')`
* Add support for `refund_payment` on `Terminal.Reader.action`
* Add support for new value `refund_payment` on enum `Terminal.Reader.action.type`

* Change `Subscription.trial_settings.end_behavior` and `Subscription.trial_settings` to be required

* Add support for `payment_link` on `Checkout.Session#list`
* Add support for `shipping_cost` on `CreditNote#create`, `CreditNote#preview_lines`, `CreditNote#preview`, `CreditNote`, `Invoice#create`, `Invoice#update`, and `Invoice`
* Add support for `amount_shipping` on `CreditNote` and `Invoice`
* Add support for `shipping_details` on `Invoice#create`, `Invoice#update`, and `Invoice`
* Change `PaymentLink.invoice_creation` to be required
* Add support for new value `America/Ciudad_Juarez` on enum `Reporting.ReportRun#create.parameters.timezone`

* Add support for `resume` method on resource `Subscription`
* Add support for `trial_settings` on `Checkout.Session#create.subscription_data`, `Subscription#create`, `Subscription#update`, and `Subscription`
* Add support for `subscription_resume_at` on `Invoice#upcomingLines` and `Invoice#upcoming`
* Change `Issuing.Cardholder#create.individual.first_name`, `Issuing.Cardholder#create.individual.last_name`, `Issuing.Cardholder#update.individual.first_name`, and `Issuing.Cardholder#update.individual.last_name` to be optional
* Change type of `Issuing.Cardholder.individual.first_name` and `Issuing.Cardholder.individual.last_name` from `string` to `nullable(string)`
* Add support for `invoice_creation` on `PaymentLink#create`, `PaymentLink#update`, and `PaymentLink`
* Add support for new value `paused` on enum `Subscription#list.status`
* Add support for new value `paused` on enum `Subscription.status`
* Add support for new values `customer.subscription.paused` and `customer.subscription.resumed` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`

* Add support for new value `BE` on enums `Checkout.Session.payment_method_options.customer_balance.bank_transfer.eu_bank_transfer.country`, `Invoice.payment_settings.payment_method_options.customer_balance.bank_transfer.eu_bank_transfer.country`, `PaymentIntent.payment_method_options.customer_balance.bank_transfer.eu_bank_transfer.country`, and `Subscription.payment_settings.payment_method_options.customer_balance.bank_transfer.eu_bank_transfer.country`
* Add support for new values `cs-CZ`, `el-GR`, `en-CZ`, and `en-GR` on enums `PaymentIntent#confirm.payment_method_options.klarna.preferred_locale`, `PaymentIntent#create.payment_method_options.klarna.preferred_locale`, and `PaymentIntent#update.payment_method_options.klarna.preferred_locale`

* Add support for `verification_session` on `EphemeralKey#create`
* Add support for new values `refund.created` and `refund.updated` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`

* Add support for `card_issuing` on `Issuing.Cardholder.individual`

* Change `Checkout.Session#create.cancel_url` to be optional
* Change type of `Checkout.Session.cancel_url` from `string` to `nullable(string)`
* Add support for new value `merchant_default` on enums `Customer#create.cash_balance.settings.reconciliation_mode` and `Customer#update.cash_balance.settings.reconciliation_mode`

* Change `Customer#list_payment_methods.type` and `PaymentMethod#list.type` to be optional

* Add support for `flow_data` on `BillingPortal.Session#create`
* Add support for `flow` on `BillingPortal.Session`

* Add support for `india_international_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
* Add support for `invoice_creation` on `Checkout.Session#create` and `Checkout.Session`
* Add support for `invoice` on `Checkout.Session`
* Add support for `metadata` on `SubscriptionSchedule#create.phases[].items[]`, `SubscriptionSchedule#update.phases[].items[]`, and `SubscriptionSchedule.phases[].items[]`

* Add support for `hosted_instructions_url` on `PaymentIntent.next_action.wechat_pay_display_qr_code`

* Remove support for resources `Order` and `Sku`
* Remove support for `cancel`, `create`, `list_line_items`, `list`, `reopen`, `retrieve`, `submit`, and `update` methods on resource `Order`
* Remove support for `create`, `delete`, `list`, `retrieve`, and `update` methods on resource `Sku`
* Change type of `Charge.refunds` from `apiList($Refund)` to `nullable(apiList($Refund))`
* Change `Charge.refunds` to be required
* Add support for `custom_text` on `Checkout.Session#create`, `Checkout.Session`, `PaymentLink#create`, `PaymentLink#update`, and `PaymentLink`
* Remove support for `amount`, `currency`, `description`, `images`, and `name` on `Checkout.Session#create.line_items[]`
* Remove support for `items` on `Checkout.Session#create.subscription_data`
* Remove support for `product` on `LineItem`
* Add support for `latest_charge` on `PaymentIntent`
* Remove support for `charges` on `PaymentIntent`
* Add support for `hosted_instructions_url` on `PaymentIntent.next_action.paynow_display_qr_code`
* Add support for new value `2022-11-15` on enum `WebhookEndpoint#create.api_version`

* Remove support for `tos_shown_and_accepted` on `Checkout.Session#create.payment_method_options.paynow`

* Add support for `reason_message` on `Issuing.Authorization.request_history[]`
* Add support for new value `webhook_error` on enum `Issuing.Authorization.request_history[].reason`

* Add support for new values `eg_tin`, `ph_tin`, and `tr_tin` on enums `Checkout.Session.customer_details.tax_ids[].type`, `Invoice.customer_tax_ids[].type`, and `Order.tax_details.tax_ids[].type`
* Add support for new values `eg_tin`, `ph_tin`, and `tr_tin` on enums `Customer#create.tax_id_data[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, `Order#create.tax_details.tax_ids[].type`, and `Order#update.tax_details.tax_ids[].type`

* Add support for `on_behalf_of` on `Checkout.Session#create.subscription_data`, `Subscription#create`, `Subscription#update`, `SubscriptionSchedule#create.default_settings`, `SubscriptionSchedule#create.phases[]`, `SubscriptionSchedule#update.default_settings`, `SubscriptionSchedule#update.phases[]`, `SubscriptionSchedule.default_settings`, `SubscriptionSchedule.phases[]`, and `Subscription`
* Add support for `tax_behavior` and `tax_code` on `Invoice#upcoming.invoice_items[]`, `Invoice#upcomingLines.invoice_items[]`, `InvoiceItem#create`, and `InvoiceItem#update`

* Add support for new values `jp_trn` and `ke_pin` on enums `Checkout.Session.customer_details.tax_ids[].type`, `Invoice.customer_tax_ids[].type`, and `Order.tax_details.tax_ids[].type`
* Add support for new values `jp_trn` and `ke_pin` on enums `Customer#create.tax_id_data[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, `Order#create.tax_details.tax_ids[].type`, and `Order#update.tax_details.tax_ids[].type`
* Add support for `tipping` on `Terminal.Reader#process_payment_intent.process_config` and `Terminal.Reader.action.process_payment_intent
.process_config`

* Add support for new values `invalid_representative_country` and `verification_failed_residential_address` on enums `Account.future_requirements.errors[].code` and `Account.requirements.errors[].code`
* Add support for `request_log_url` on `Invoice.last_finalization_error`, `PaymentIntent.last_payment_error`, `SetupAttempt.setup_error`, `SetupIntent.last_setup_error`, and `StripeError`
* Add support for `network_data` on `Issuing.Authorization`

* Add support for new value `bank_of_china` on enums `Charge.payment_method_details.fpx.bank`, `PaymentIntent#confirm.payment_method_data.fpx.bank`, `PaymentIntent#create.payment_method_data.fpx.bank`, `PaymentIntent#update.payment_method_data.fpx.bank`, `PaymentMethod#create.fpx.bank`, `PaymentMethod.fpx.bank`, `SetupIntent#confirm.payment_method_data.fpx.bank`, `SetupIntent#create.payment_method_data.fpx.bank`, and `SetupIntent#update.payment_method_data.fpx.bank`

* Add support for new value `invalid_dob_age_under_18` on enums `Account.future_requirements.errors[].code` and `Account.requirements.errors[].code`
* Add support for new values `America/Nuuk`, `Europe/Kyiv`, and `Pacific/Kanton` on enum `Reporting.ReportRun#create.parameters.timezone`
* Add support for `klarna` on `SetupAttempt.payment_method_details`

## 2022-08-04

- Remove support for resources `AlipayAccount`, `BitcoinReceiver`, `BitcoinTransaction`, `IssuerFraudRecord`, `Recipient`, and `ThreeDSecure`
- Add support for `list_line_items` method on resource `Checkout.Session`
- Remove support for `list` method on resource `LineItem`
- Add support for new value `invalid_tos_acceptance` on enums `Account.future_requirements.errors[].code`, `Account.requirements.errors[].code`, `Capability.future_requirements.errors[].code`, `Capability.requirements.errors[].code`, `Person.future_requirements.errors[].code`, and `Person.requirements.errors[].code`
- Remove support for `recipient` on `Card`
- Add support for `shipping_cost` and `shipping_details` on `Checkout.Session`
- Remove support for `shipping_rate` and `shipping` on `Checkout.Session`
- Add support for `validate` on `Customer#create`, `Customer#update`, and `PaymentSource#create`
- Remove support for `trial_end` on `Customer#update`
- Remove support for `default_currency` on `Customer`
- Add support for new value `design_rejected` on enum `Issuing.Card.cancellation_reason`
- Remove support for `redirect_url` on `LoginLink#create`
- Add support for new value `2022-08-01` on enum `WebhookEndpoint#create.api_version`
- Remove support for values `order.payment_failed`, `order.payment_succeeded`, `order.updated`, `order_return.created`, `transfer.failed`, and `transfer.paid` from enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Add support for `customer_balance` on `Checkout.Session#create.payment_method_options` and `Checkout.Session.payment_method_options`
- Add support for new value `customer_balance` on enum `Checkout.Session#create.payment_method_types[]`
- Add support for new values `en-CA` and `fr-CA` on enums `Order#create.payment.settings.payment_method_options.klarna.preferred_locale`, `Order#update.payment.settings.payment_method_options.klarna.preferred_locale`, `PaymentIntent#confirm.payment_method_options.klarna.preferred_locale`, `PaymentIntent#create.payment_method_options.klarna.preferred_locale`, and `PaymentIntent#update.payment_method_options.klarna.preferred_locale`
- Add support for new value `exempted` on enums `Charge.payment_method_details.card.three_d_secure.result` and `SetupAttempt.payment_method_details.card.three_d_secure.result`
- Remove support for resource `InstallmentsOptions`
- Add support for `installments` on `Invoice.payment_settings.payment_method_options.card`
- Add support for new resource `InstallmentsOptions`
- Add support for `installments` on `Checkout.Session#create.payment_method_options.card`, `Checkout.Session.payment_method_options.card`, `Invoice#create.payment_settings.payment_method_options.card`, `Invoice#update.payment_settings.payment_method_options.card`, and `PaymentIntentTypeSpecificPaymentMethodOptionsClient`
- Add support for `default_mandate` on `Invoice#create.payment_settings`, `Invoice#update.payment_settings`, and `Invoice.payment_settings`
- Add support for `mandate` on `Invoice#pay`
- Add support for `product_data` on `Order#create.line_items[]` and `Order#update.line_items[]`
- Add support for `default_currency` and `invoice_credit_balance` on `Customer`
- Add support for `currency` on `Invoice#create`
- Add support for `blik_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
- Add support for `blik` on `Charge.payment_method_details`, `Mandate.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod#update`, `PaymentMethod`, `SetupAttempt.payment_method_details`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#confirm.payment_method_options`, `SetupIntent#create.payment_method_data`, `SetupIntent#create.payment_method_options`, `SetupIntent#update.payment_method_data`, `SetupIntent#update.payment_method_options`, and `SetupIntent.payment_method_options`
- Add support for new value `blik` on enum `Checkout.Session#create.payment_method_types[]`
- Add support for new value `blik` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
- Add support for new value `blik` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `SetupIntent#confirm.payment_method_data.type`, `SetupIntent#create.payment_method_data.type`, and `SetupIntent#update.payment_method_data.type`
- Add support for new value `blik` on enums `PaymentLink#create.payment_method_types[]`, `PaymentLink#update.payment_method_types[]`, and `PaymentLink.payment_method_types[]`
- Add support for new value `blik` on enum `PaymentMethod#create.type`
- Add support for new value `blik` on enum `PaymentMethod.type`
- Change type of `Checkout.Session#create.consent_collection.promotions`, `Checkout.Session.consent_collection.promotions`, `PaymentLink#create.consent_collection.promotions`, and `PaymentLink.consent_collection.promotions` from `literal('auto')` to `enum('auto'|'none')`
- Change type of `Transfer.source_type` from `nullable(string)` to `string`
- Change `Transfer.source_type` to be optional
- Add support for `customer_details` on `Checkout.Session#list`
- Add support for `currency` on `Checkout.Session#create`, `Invoice#upcomingLines`, `Invoice#upcoming`, `PaymentLink#create`, `Subscription#create`, `SubscriptionSchedule#create.phases[]`, `SubscriptionSchedule#update.phases[]`, `SubscriptionSchedule.phases[]`, and `Subscription`
- Add support for `currency_options` on `Checkout.Session#create.shipping_options[].shipping_rate_data.fixed_amount`, `Coupon#create`, `Coupon#update`, `Coupon`, `Order#create.shipping_cost.shipping_rate_data.fixed_amount`, `Order#update.shipping_cost.shipping_rate_data.fixed_amount`, `Price#create`, `Price#update`, `Price`, `Product#create.default_price_data`, `PromotionCode#create.restrictions`, `PromotionCode.restrictions`, `ShippingRate#create.fixed_amount`, and `ShippingRate.fixed_amount`
- Change `LineItem.amount_discount` and `LineItem.amount_tax` to be required
- Add support for `restrictions` on `PromotionCode#update`
- Add support for `fixed_amount` and `tax_behavior` on `ShippingRate#update`
- Add support for `currency`, `customer`, and `origin` on `Refund#create`
- Add support for `customer` on `Checkout.Session#list`
- Add support for new values `financial_connections.account.created`, `financial_connections.account.deactivated`, `financial_connections.account.disconnected`, `financial_connections.account.reactivated`, and `financial_connections.account.refreshed_balance` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Add support for `deliver_card`, `fail_card`, `return_card`, and `ship_card` test helper methods on resource `Issuing.Card`
- Change type of `PaymentLink#create.payment_method_types[]`, `PaymentLink#update.payment_method_types[]`, and `PaymentLink.payment_method_types[]` from `literal('card')` to `enum`

## 2022-06-26

- Add support for `hosted_regulatory_receipt_url` on `Treasury.ReceivedCredit` and `Treasury.ReceivedDebit`
- Remove support for value `treasury.received_credit.reversed` from enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`
- Add support for `capture_method` on `PaymentIntent#confirm` and `PaymentIntent#update`
- Change `Price.custom_unit_amount` to be required
- Add support for `reversal_details` on `Treasury.ReceivedCredit` and `Treasury.ReceivedDebit`
- Add support for `debit_reversal` on `Treasury.ReceivedDebit.linked_flows`
- Add support for `promptpay_payments` on `Account#create.capabilities`, `Account#update.capabilities`, and `Account.capabilities`
- Add support for `promptpay` on `Charge.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#create.payment_method_data`, and `SetupIntent#update.payment_method_data`
- Add support for new value `promptpay` on enum `Checkout.Session#create.payment_method_types[]`
- Add support for `subtotal_excluding_tax` on `CreditNote` and `Invoice`
- Add support for `amount_excluding_tax` and `unit_amount_excluding_tax` on `CreditNoteLineItem` and `InvoiceLineItem`
- Add support for new value `promptpay` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
- Add support for `rendering_options` on `Invoice#create` and `Invoice#update`
- Add support for new value `promptpay` on enums `Invoice#create.payment_settings.payment_method_types[]`, `Invoice#update.payment_settings.payment_method_types[]`, `Invoice.payment_settings.payment_method_types[]`, `Subscription#create.payment_settings.payment_method_types[]`, `Subscription#update.payment_settings.payment_method_types[]`, and `Subscription.payment_settings.payment_method_types[]`
- Add support for `total_excluding_tax` on `Invoice`
- Add support for `automatic_payment_methods` on `Order.payment.settings`
- Add support for new value `promptpay` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `SetupIntent#confirm.payment_method_data.type`, `SetupIntent#create.payment_method_data.type`, and `SetupIntent#update.payment_method_data.type`
- Add support for `promptpay_display_qr_code` on `PaymentIntent.next_action`
- Add support for new value `promptpay` on enum `PaymentMethod#create.type`
- Add support for new value `promptpay` on enum `PaymentMethod.type`
- Add support for `fund_cash_balance` test helper method on resource `Customer`
- Remove support for `fund_cash_balance` test helper method on resource `CustomerBalanceTransaction`
- Remove support for `list_funding_instructions` method on resource `Customer`
- Add support for `fund_cash_balance` test helper method on resource `CustomerBalanceTransaction`
- Remove support for `subtotal_excluding_tax` on `CreditNote` and `Invoice`
- Remove support for `amount_excluding_tax` and `unit_amount_excluding_tax` on `CreditNoteLineItem` and `InvoiceLineItem`
- Remove support for `rendering_options` on `Invoice#create` and `Invoice#update`
- Remove support for `total_excluding_tax` on `Invoice`
- Add support for `list_funding_instructions` method on resource `Customer`
- Add support for `statement_descriptor_prefix_kana` and `statement_descriptor_prefix_kanji` on `Account#create.settings.card_payments`, `Account#update.settings.card_payments`, `Account.settings.card_payments`, and `Account.settings.payments`
- Add support for `statement_descriptor_suffix_kana` and `statement_descriptor_suffix_kanji` on `Checkout.Session#create.payment_method_options.card`, `Checkout.Session.payment_method_options.card`, `PaymentIntent#confirm.payment_method_options.card`, `PaymentIntent#create.payment_method_options.card`, `PaymentIntent#update.payment_method_options.card`, and `PaymentIntent.payment_method_options.card`
- Add support for `subtotal_excluding_tax` and `total_excluding_tax` on `CreditNote` and `Invoice`
- Add support for `amount_excluding_tax` and `unit_amount_excluding_tax` on `CreditNoteLineItem` and `InvoiceLineItem`
- Add support for `rendering_options` on `Customer.invoice_settings`, `Invoice#create`, `Invoice#update`, and `Invoice`
- No differences
- Change type of `Customer#create.invoice_settings.rendering_options` and `Customer#update.invoice_settings.rendering_options` from `rendering_options_param` to `emptyStringable(rendering_options_param)`
- Add support for `treasury` on `Account#create.settings`, `Account#update.settings`, and `Account.settings`
- Add support for `rendering_options` on `Customer#create.invoice_settings` and `Customer#update.invoice_settings`
- Add support for `custom_unit_amount` on `Price#create` and `Price`
- Remove support for `installments` on `Checkout.Session.payment_method_options.card`
- Add support for `eu_bank_transfer` on `Customer#create_funding_instructions.bank_transfer`, `Invoice#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent.payment_method_options.customer_balance.bank_transfer`, `Subscription#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Subscription#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, and `Subscription.payment_settings.payment_method_options.customer_balance.bank_transfer`
- Change type of `Customer#create_funding_instructions.bank_transfer.requested_address_types[]` from `literal('zengin')` to `enum('iban'|'sort_code'|'spei'|'zengin')`
- Change type of `Customer#create_funding_instructions.bank_transfer.type`, `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent.next_action.display_bank_transfer_instructions.type`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.type` from `literal('jp_bank_transfer')` to `enum('eu_bank_transfer'|'gb_bank_transfer'|'jp_bank_transfer'|'mx_bank_transfer')`
- Add support for `iban`, `sort_code`, and `spei` on `FundingInstructions.bank_transfer.financial_addresses[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[]`
- Add support for new values `bacs`, `fps`, and `spei` on enums `FundingInstructions.bank_transfer.financial_addresses[].supported_networks[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].supported_networks[]`
- Add support for new values `sort_code` and `spei` on enums `FundingInstructions.bank_transfer.financial_addresses[].type` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].type`
- Change type of `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.requested_address_types[]` from `literal('zengin')` to `enum`
- Add support for `attach_to_self` on `SetupAttempt`, `SetupIntent#create`, `SetupIntent#list`, and `SetupIntent#update`
- Add support for `flow_directions` on `SetupAttempt`, `SetupIntent#create`, and `SetupIntent#update`
- Add support for `affirm`, `afterpay_clearpay`, `au_becs_debit`, `bacs_debit`, `bancontact`, `eps`, `fpx`, `giropay`, `grabpay`, `ideal`, `klarna`, `p24`, `paynow`, `sepa_debit`, and `sofort` on `Checkout.Session#create.payment_method_options`
- Add support for `card` on `Checkout.Session#create.payment_method_options` and `Checkout.Session.payment_method_options`
- Add support for `setup_future_usage` on `Checkout.Session#create.payment_method_options.acss_debit`, `Checkout.Session#create.payment_method_options.alipay`, `Checkout.Session#create.payment_method_options.boleto`, `Checkout.Session#create.payment_method_options.konbini`, `Checkout.Session#create.payment_method_options.oxxo`, `Checkout.Session#create.payment_method_options.us_bank_account`, `Checkout.Session#create.payment_method_options.wechat_pay`, `Checkout.Session.payment_method_options.acss_debit`, `Checkout.Session.payment_method_options.affirm`, `Checkout.Session.payment_method_options.afterpay_clearpay`, `Checkout.Session.payment_method_options.alipay`, `Checkout.Session.payment_method_options.au_becs_debit`, `Checkout.Session.payment_method_options.bacs_debit`, `Checkout.Session.payment_method_options.bancontact`, `Checkout.Session.payment_method_options.boleto`, `Checkout.Session.payment_method_options.eps`, `Checkout.Session.payment_method_options.fpx`, `Checkout.Session.payment_method_options.giropay`, `Checkout.Session.payment_method_options.grabpay`, `Checkout.Session.payment_method_options.ideal`, `Checkout.Session.payment_method_options.klarna`, `Checkout.Session.payment_method_options.konbini`, `Checkout.Session.payment_method_options.oxxo`, `Checkout.Session.payment_method_options.p24`, `Checkout.Session.payment_method_options.paynow`, `Checkout.Session.payment_method_options.sepa_debit`, `Checkout.Session.payment_method_options.sofort`, and `Checkout.Session.payment_method_options.us_bank_account`
- Remove support for `eu_bank_transfer` on `Customer#create_funding_instructions.bank_transfer`, `Invoice#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent.payment_method_options.customer_balance.bank_transfer`, `Subscription#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Subscription#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, and `Subscription.payment_settings.payment_method_options.customer_balance.bank_transfer`
- Change type of `Customer#create_funding_instructions.bank_transfer.requested_address_types[]` from `enum('iban'|'sort_code'|'spei'|'zengin')` to `literal('zengin')`
- Change type of `Customer#create_funding_instructions.bank_transfer.type`, `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent.next_action.display_bank_transfer_instructions.type`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.type` from `enum('eu_bank_transfer'|'gb_bank_transfer'|'jp_bank_transfer'|'mx_bank_transfer')` to `literal('jp_bank_transfer')`
- Remove support for `iban`, `sort_code`, and `spei` on `FundingInstructions.bank_transfer.financial_addresses[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[]`
- Remove support for values `bacs`, `fps`, and `spei` from enums `FundingInstructions.bank_transfer.financial_addresses[].supported_networks[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].supported_networks[]`
- Remove support for values `sort_code` and `spei` from enums `FundingInstructions.bank_transfer.financial_addresses[].type` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].type`
- Change type of `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.requested_address_types[]` from `enum` to `literal('zengin')`
- Change `PaymentMethod.us_bank_account.networks` and `SetupIntent.flow_directions` to be required
- Add support for `affirm` on `Checkout.Session.payment_method_options`
- Add support for `bancontact`, `ideal`, `p24`, and `sofort` on `Checkout.Session.payment_method_options`
- Add support for `eu_bank_transfer` on `Customer#create_funding_instructions.bank_transfer`, `Invoice#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Invoice.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer`, `PaymentIntent.payment_method_options.customer_balance.bank_transfer`, `Subscription#create.payment_settings.payment_method_options.customer_balance.bank_transfer`, `Subscription#update.payment_settings.payment_method_options.customer_balance.bank_transfer`, and `Subscription.payment_settings.payment_method_options.customer_balance.bank_transfer`
- Change type of `Customer#create_funding_instructions.bank_transfer.requested_address_types[]` from `literal('zengin')` to `enum('iban'|'sort_code'|'spei'|'zengin')`
- Change type of `Customer#create_funding_instructions.bank_transfer.type`, `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.type`, `PaymentIntent.next_action.display_bank_transfer_instructions.type`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.type` from `literal('jp_bank_transfer')` to `enum('eu_bank_transfer'|'gb_bank_transfer'|'jp_bank_transfer'|'mx_bank_transfer')`
- Add support for `iban`, `sort_code`, and `spei` on `FundingInstructions.bank_transfer.financial_addresses[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[]`
- Add support for new values `bacs`, `fps`, and `spei` on enums `FundingInstructions.bank_transfer.financial_addresses[].supported_networks[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].supported_networks[]`
- Add support for new values `sort_code` and `spei` on enums `FundingInstructions.bank_transfer.financial_addresses[].type` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].type`
- Change type of `Order#create.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Order#update.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `Order.payment.settings.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#confirm.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#create.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, `PaymentIntent#update.payment_method_options.customer_balance.bank_transfer.requested_address_types[]`, and `PaymentIntent.payment_method_options.customer_balance.bank_transfer.requested_address_types[]` from `literal('zengin')` to `enum`
- Add support for `radar_options` on `Charge#create`, `Charge`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create`, `PaymentIntent#update.payment_method_data`, `PaymentMethod#create`, `PaymentMethod`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#create.payment_method_data`, and `SetupIntent#update.payment_method_data`

## 2022-05-06

- Add support for `description` on `Checkout.Session#create.subscription_data`, `Subscription#create`, `Subscription#update`, and `Subscription`
- Add support for new resource `FinancialConnections.AccountOwnership`
- Remove support for resources `OrderItem` and `OrderReturn`
- Add support for `cancel`, `list_line_items`, `reopen`, and `submit` methods on resource `Order`
- Remove support for `pay` and `return_order` methods on resource `Order`
- Remove support for `order` on `Charge`
- Change type of `Charge.shipping.name`, `Checkout.Session.shipping.name`, `Customer.shipping.name`, `Invoice.customer_shipping.name`, `PaymentIntent.shipping.name`, `ShippingDetails.name`, and `Source.source_order.shipping.name` from `nullable(string)` to `string`
- Change type of `FinancialConnections.Account.ownership` from `$Ownership` to `$FinancialConnections.AccountOwnership`
- Add support for `id` and `object` on `FinancialConnections.AccountOwner`
- Add support for `amount_discount`, `amount_tax`, and `product` on `LineItem`
- Add support for `automatic_tax`, `billing_details`, `description`, `discounts`, `ip_address`, `line_items`, `payment`, `shipping_cost`, `shipping_details`, and `tax_details` on `Order#create`, `Order#update`, and `Order`
- Remove support for `coupon` on `Order#create` and `Order#update`
- Remove support for `email` and `items` on `Order#create` and `Order`
- Remove support for `shipping` on `Order#create`, `Order#update`, and `Order`
- Remove support for `created`, `ids`, and `upstream_ids` on `Order#list`
- Remove support for `status` on `Order#list` and `Order#update`
- Remove support for `status_transitions` on `Order#list` and `Order`
- Add support for `currency` and `customer` on `Order#update`
- Remove support for `selected_shipping_method` on `Order#update` and `Order`
- Add support for `amount_subtotal`, `amount_total`, and `total_details` on `Order`
- Remove support for `amount_returned`, `amount`, `application_fee`, `charge`, `external_coupon_code`, `returns`, `shipping_methods`, `updated`, and `upstream_id` on `Order`
- Change type of `Order.application` from `string` to `expandable($Application)`
- Change type of `Order.status` from `string` to `enum`
- Add support for `instructions_email` on `Refund#create` and `Refund`
- Add support for new resources `FinancialConnections.AccountOwner`, `FinancialConnections.Account`, and `FinancialConnections.Session`
- Add support for `registered_address` on `Account#create.individual`, `Account#update.individual`, `Person#create`, `Person#update`, `Person`, `Token#create.account.individual`, and `Token#create.person`
- Add support for `financial_connections` on `Checkout.Session#create.payment_method_options.us_bank_account`, `Checkout.Session.payment_method_options.us_bank_account`, `Invoice#create.payment_settings.payment_method_options.us_bank_account`, `Invoice#update.payment_settings.payment_method_options.us_bank_account`, `Invoice.payment_settings.payment_method_options.us_bank_account`, `PaymentIntent#confirm.payment_method_options.us_bank_account`, `PaymentIntent#create.payment_method_options.us_bank_account`, `PaymentIntent#update.payment_method_options.us_bank_account`, `PaymentIntent.payment_method_options.us_bank_account`, `SetupIntent#confirm.payment_method_options.us_bank_account`, `SetupIntent#create.payment_method_options.us_bank_account`, `SetupIntent#update.payment_method_options.us_bank_account`, `SetupIntent.payment_method_options.us_bank_account`, `Subscription#create.payment_settings.payment_method_options.us_bank_account`, `Subscription#update.payment_settings.payment_method_options.us_bank_account`, and `Subscription.payment_settings.payment_method_options.us_bank_account`
- Add support for `financial_connections_account` on `PaymentIntent#confirm.payment_method_data.us_bank_account`, `PaymentIntent#create.payment_method_data.us_bank_account`, `PaymentIntent#update.payment_method_data.us_bank_account`, `PaymentMethod#create.us_bank_account`, `PaymentMethod.us_bank_account`, `SetupIntent#confirm.payment_method_data.us_bank_account`, `SetupIntent#create.payment_method_data.us_bank_account`, and `SetupIntent#update.payment_method_data.us_bank_account`
- Add support for `default_price_data` on `Product#create`
- Add support for `default_price` on `Product#update` and `Product`
- Change type of `PaymentIntent.amount_details.tip.amount` from `nullable(integer)` to `integer`
- Change `PaymentIntent.amount_details.tip.amount` to be optional
- Add support for `payment_method_data` on `SetupIntent#confirm`, `SetupIntent#create`, and `SetupIntent#update`
- Add support for new resource `CashBalance`
- Add support for `cash_balance` on `Customer`
- Add support for new value `eu_oss_vat` on enums `Checkout.Session.customer_details.tax_ids[].type`, `Invoice.customer_tax_ids[].type`, and `TaxId.type`
- Add support for new value `eu_oss_vat` on enums `Customer#create.tax_id_data[].type`, `Invoice#upcoming.customer_details.tax_ids[].type`, `Invoice#upcomingLines.customer_details.tax_ids[].type`, and `TaxId#create.type`
- Add support for `application` on `Invoice`, `Quote`, `SubscriptionSchedule`, and `Subscription`
- Change type of `Checkout.Session#create.payment_method_options.konbini.expires_after_days` from `emptyStringable(integer)` to `integer`
- Change type of `BillingPortal.Configuration.application` from `$Application` to `deletable($Application)`
- Add support for `alipay` on `Checkout.Session#create.payment_method_options` and `Checkout.Session.payment_method_options`
- Add support for `expire` test helper method on resource `Refund`
- Change `Issuing.Dispute#create.transaction` to be optional
- Add support for `create_funding_instructions` method on resource `Customer`
- Remove support for `create` method on resource `FundingInstructions`
- Change type of `BillingPortal.Configuration.application` from `string` to `expandable($Application)`
- Remove support for `list` method on resource `FundingInstructions`
- Add support for `amount_details` on `PaymentIntent`
- Add support for `verifone_p400` on `Terminal.Configuration#create`, `Terminal.Configuration#update`, and `Terminal.Configuration`
- Remove support for `verifone_P400` on `Terminal.Configuration#create`, `Terminal.Configuration#update`, and `Terminal.Configuration`
- Add support for new resource `Terminal.Configuration`
- Change type of `FundingInstructions.bank_transfer.financial_addresses[].supported_networks[]` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].supported_networks[]` from `literal('zengin')` to `enum('sepa'|'zengin')`
- Change type of `FundingInstructions.bank_transfer.financial_addresses[].type` and `PaymentIntent.next_action.display_bank_transfer_instructions.financial_addresses[].type` from `literal('zengin')` to `enum('iban'|'zengin')`
- Change type of `FundingInstructions.bank_transfer.type` from `literal('jp_bank_transfer')` to `enum('eu_bank_transfer'|'jp_bank_transfer')`
- Add support for `configuration_overrides` on `Terminal.Location#create`, `Terminal.Location#update`, and `Terminal.Location`
- Add support for new resource `FundingInstructions`
- Add support for `increment_authorization` method on resource `PaymentIntent`
- Add support for `customer_balance` on `Charge.payment_method_details`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, and `PaymentMethod`
- Add support for `incremental_authorization_supported` on `Charge.payment_method_details.card_present`
- Add support for `cash_balance` on `Customer#create` and `Customer#update`
- Add support for new value `customer_balance` on enums `Customer#list_payment_methods.type` and `PaymentMethod#list.type`
- Add support for new value `customer_balance` on enums `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, and `PaymentIntent#update.payment_method_data.type`
- Add support for `request_incremental_authorization_support` on `PaymentIntent#confirm.payment_method_options.card_present`, `PaymentIntent#create.payment_method_options.card_present`, `PaymentIntent#update.payment_method_options.card_present`, and `PaymentIntent.payment_method_options.card_present`
- Add support for `display_bank_transfer_instructions` on `PaymentIntent.next_action`
- Add support for new value `customer_balance` on enum `PaymentMethod#create.type`
- Add support for new value `customer_balance` on enum `PaymentMethod.type`
- Add support for new value `cash_balance.funds_available` on enums `WebhookEndpoint#create.enabled_events[]` and `WebhookEndpoint#update.enabled_events[]`

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
