#CHANGELOG

## Changelog

## 2024-03-21
* Add support for new values `forwarding_api_inactive`, `forwarding_api_invalid_parameter`, `forwarding_api_upstream_connection_error`, and `forwarding_api_upstream_connection_timeout` on enums `Invoice.last_finalization_error.code`, `PaymentIntent.last_payment_error.code`, `SetupAttempt.setup_error.code`, `SetupIntent.last_setup_error.code`, and `StripeError.code`
* Add support for `mobilepay` on `Charge.payment_method_details`, `ConfirmationToken.payment_method_preview`, `ConfirmationToken.testHelpers#create.payment_method_data`, `PaymentIntent#confirm.payment_method_data`, `PaymentIntent#confirm.payment_method_options`, `PaymentIntent#create.payment_method_data`, `PaymentIntent#create.payment_method_options`, `PaymentIntent#update.payment_method_data`, `PaymentIntent#update.payment_method_options`, `PaymentIntent.payment_method_options`, `PaymentMethod#create`, `PaymentMethod`, `SetupIntent#confirm.payment_method_data`, `SetupIntent#create.payment_method_data`, and `SetupIntent#update.payment_method_data`
* Add support for new value `mobilepay` on enums `ConfirmationToken.testHelpers#create.payment_method_data.type`, `PaymentIntent#confirm.payment_method_data.type`, `PaymentIntent#create.payment_method_data.type`, `PaymentIntent#update.payment_method_data.type`, `SetupIntent#confirm.payment_method_data.type`, `SetupIntent#create.payment_method_data.type`, and `SetupIntent#update.payment_method_data.type`
* Add support for new value `mobilepay` on enums `ConfirmationToken.payment_method_preview.type` and `PaymentMethod.type`
* Add support for new value `mobilepay` on enums `Customer#list_payment_methods.type`, `PaymentMethod#create.type`, and `PaymentMethod#list.type`

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