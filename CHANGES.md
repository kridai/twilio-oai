twilio-oai changelog
====================
[2021-12-01] Version 1.23.2
---------------------------
**Conversations**
- Add `Service Webhook Configuration` resource

**Flex**
- Adding `flex_insights_drilldown` and `flex_url` objects to Flex Configuration

**Messaging**
- Update us_app_to_person endpoints to remove beta feature flag based access

**Supersim**
- Add IP Commands resource

**Verify**
- Add optional `factor_friendly_name` parameter to the create access token endpoint.

**Video**
- Add maxParticipantDuration param to Rooms

**Twiml**
- Unrevert Add supported SSML children to `<emphasis>`, `<lang>`, `<p>`, `<prosody>`, `<s>`, and `<w>`.
- Revert Add supported SSML children to `<emphasis>`, `<lang>`, `<p>`, `<prosody>`, `<s>`, and `<w>`.


[2021-11-17] Version 1.23.1
---------------------------
**Frontline**
- Added `is_available` to User's resource

**Messaging**
- Added GET vetting API

**Verify**
- Add `WHATSAPP` to the attempts API.
- Allow to update `config.notification_platform` from `none` to `apn` or `fcm` and viceversa for Verify Push
- Add `none` as a valid `config.notification_platform` value for Verify Push

**Twiml**
- Add supported SSML children to `<emphasis>`, `<lang>`, `<p>`, `<prosody>`, `<s>`, and `<w>`.


[2021-11-03] Version 1.23.0
---------------------------
**Library - Chore**
- [PR #46](https://github.com/twilio/twilio-oai/pull/46): migrate from travis over to gh actions. Thanks to [@shwetha-manvinkurke](https://github.com/shwetha-manvinkurke)!

**Api**
- Updated `media_url` property to be treated as PII

**Messaging**
- Added a new enum for brand registration status named DELETED **(breaking change)**
- Add a new K12_EDUCATION use case in us_app_to_person_usecase api transaction
- Added a new enum for brand registration status named IN_REVIEW

**Serverless**
- Add node14 as a valid Build runtime

**Verify**
- Fix typos in Verify Push Factor documentation for the `config.notification_token` parameter.
- Added `TemplateCustomSubstitutions` on verification creation
- Make `TemplateSid` parameter public for Verification resource and `DefaultTemplateSid` parameter public for Service resource. **(breaking change)**


[2021-10-18] Version 1.22.0
---------------------------
**Api**
- Corrected enum values for `emergency_address_status` values in `/IncomingPhoneNumbers` response. **(breaking change)**
- Clarify `emergency_address_status` values in `/IncomingPhoneNumbers` response.

**Messaging**
- Add PUT and List brand vettings api
- Removes beta feature flag based visibility for us_app_to_person_registered and usecase field.Updates test cases to add POLITICAL usecase. **(breaking change)**
- Add brand_feedback as optional field to BrandRegistrations

**Video**
- Add `AudioOnly` to create room


[2021-10-06] Version 1.21.0
---------------------------
**Library - Fix**
- [PR #44](https://github.com/twilio/twilio-oai/pull/44): fix naming of params. Thanks to [@shwetha-manvinkurke](https://github.com/shwetha-manvinkurke)!

**Api**
- Add `emergency_address_status` attribute to `/IncomingPhoneNumbers` response.
- Add `siprec` resource

**Conversations**
- Added attachment parameters in configuration for `NewMessage` type of push notifications

**Flex**
- Adding `flex_insights_hr` object to Flex Configuration

**Numbers**
- Add API endpoint for Bundle ReplaceItems resource
- Add API endpoint for Bundle Copies resource

**Serverless**
- Add domain_base field to Service response

**Taskrouter**
- Add `If-Match` Header based on ETag for Worker Delete **(breaking change)**
- Add `If-Match` Header based on Etag for Reservation Update
- Add `If-Match` Header based on ETag for Worker Update
- Add `If-Match` Header based on ETag for Worker Delete
- Add `ETag` as Response Header to Worker

**Trunking**
- Added `transfer_caller_id` property on Trunks.

**Verify**
- Document new pilot `whatsapp` channel.


[2021-09-22] Version 1.20.3
---------------------------
**Events**
- Add segment sink

**Messaging**
- Add post_approval_required attribute in GET us_app_to_person_usecase api response
- Add Identity Status, Russell 3000, Tax Exempt Status and Should Skip SecVet fields for Brand Registrations
- Add Should Skip Secondary Vetting optional flag parameter to create Brand API


[2021-09-08] Version 1.20.2
---------------------------
**Api**
- Revert adding `siprec` resource
- Add `siprec` resource

**Messaging**
- Add 'mock' as an optional field to brand_registration api
- Add 'mock' as an optional field to us_app_to_person api
- Adds more Use Cases in us_app_to_person_usecase api transaction and updates us_app_to_person_usecase docs

**Verify**
- Verify List Templates API endpoint added.


[2021-08-25] Version 1.20.1
---------------------------
**Api**
- Add Programmabled Voice SIP Refer call transfers (`calls-transfers`) to usage records
- Add Flex Voice Usage category (`flex-usage`) to usage records

**Conversations**
- Add `Order` query parameter to Message resource read operation

**Insights**
- Added `partial` to enum processing_state_request
- Added abnormal session filter in Call Summaries

**Messaging**
- Add brand_registration_sid as an optional query param for us_app_to_person_usecase api

**Pricing**
- add trunking_numbers resource (v2)
- add trunking_country resource (v2)

**Verify**
- Changed to private beta the `TemplateSid` optional parameter on Verification creation.
- Added the optional parameter `Order` to the list Challenges endpoint to define the list order.


[2021-08-11] Version 1.20.0
---------------------------
**Api**
- Corrected the `price`, `call_sid_to_coach`, and `uri` data types for Conference, Participant, and Recording **(breaking change)**
- Made documentation for property `time_limit` in the call api public. **(breaking change)**
- Added `domain_sid` in sip_credential_list_mapping and sip_ip_access_control_list_mapping APIs **(breaking change)**

**Insights**
- Added new endpoint to fetch Call Summaries

**Messaging**
- Add brand_type field to a2p brand_registration api
- Revert brand registration api update to add brand_type field
- Add brand_type field to a2p brand_registration api

**Taskrouter**
- Add `X-Rate-Limit-Limit`, `X-Rate-Limit-Remaining`, and `X-Rate-Limit-Config` as Response Headers to all TaskRouter endpoints

**Verify**
- Add `TemplateSid` optional parameter on Verification creation.
- Include `whatsapp` as a channel type in the verifications API.


[2021-07-28] Version 1.19.1
---------------------------
**Conversations**
- Expose ParticipantConversations resource

**Taskrouter**
- Adding `links` to the activity resource

**Verify**
- Added a `Version` to Verify Factors `Webhooks` to add new fields without breaking old Webhooks.


[2021-07-14] Version 1.19.0
---------------------------
**Library - Chore**
- [PR #40](https://github.com/twilio/twilio-oai/pull/40): make sure spectral is installed. Thanks to [@thinkingserious](https://github.com/thinkingserious)!
- [PR #39](https://github.com/twilio/twilio-oai/pull/39): add spectral target alias test. Thanks to [@childish-sambino](https://github.com/childish-sambino)!

**Conversations**
- Changed `last_read_message_index` and `unread_messages_count` type in User Conversation's resource **(breaking change)**
- Expose UserConversations resource

**Messaging**
- Add brand_score field to brand registration responses


[2021-06-30] Version 1.18.0
---------------------------
**Conversations**
- Read-only Conversation Email Binding property `binding`

**Supersim**
- Add Billing Period resource for the Super Sim Pilot
- Add List endpoint to Billing Period resource for Super Sim Pilot
- Add Fetch endpoint to Billing Period resource for Super Sim Pilot

**Taskrouter**
- Update `transcribe` & `transcription_configuration` form params in Reservation update endpoint to have private visibility **(breaking change)**
- Add `transcribe` & `transcription_configuration` form params to Reservation update endpoint

**Twiml**
- Add `modify` event to `statusCallbackEvent` for `<Conference>`.


[2021-06-16] Version 1.17.0
---------------------------
**Library - Feature**
- [PR #38](https://github.com/twilio/twilio-oai/pull/38): add sidKey, if present, to the OpenAPI docs. Thanks to [@childish-sambino](https://github.com/childish-sambino)!

**Library - Chore**
- [PR #37](https://github.com/twilio/twilio-oai/pull/37): refactor the Twilio vendor extensions into single object. Thanks to [@childish-sambino](https://github.com/childish-sambino)!

**Api**
- Update `status` enum for Messages to include 'canceled'
- Update `update_status` enum for Messages to include 'canceled'

**Trusthub**
- Corrected the sid for policy sid in customer_profile_evaluation.json and trust_product_evaluation.json **(breaking change)**


[2021-06-02] Version 1.16.1
---------------------------
**Events**
- join Sinks and Subscriptions service

**Verify**
- Improved the documentation of `challenge` adding the maximum and minimum expected lengths of some fields.
- Improve documentation regarding `notification` by updating the documentation of the field `ttl`.


[2021-05-19] Version 1.16.0
---------------------------
**Events**
- add query param to return types filtered by Schema Id
- Add query param to return sinks filtered by status
- Add query param to return sinks used/not used by a subscription

**Messaging**
- Add fetch and delete instance endpoints to us_app_to_person api **(breaking change)**
- Remove delete list endpoint from us_app_to_person api **(breaking change)**
- Update read list endpoint to return a list of us_app_to_person compliance objects **(breaking change)**
- Add `sid` field to Preregistered US App To Person response

**Supersim**
- Mark `unique_name` in Sim, Fleet, NAP resources as not PII

**Video**
- [Composer] GA maturity level


[2021-05-05] Version 1.15.0
---------------------------
**Api**
- Corrected the data types for feedback summary fields **(breaking change)**
- Update the conference participant create `from` and `to` param to be endpoint type for supporting client identifier and sip address

**Bulkexports**
- promoting API maturity to GA

**Events**
- Add endpoint to update description in sink
- Remove beta-feature account flag

**Messaging**
- Update `status` field in us_app_to_person api to `campaign_status` **(breaking change)**

**Verify**
- Improve documentation regarding `push` factor and include extra information about `totp` factor.


[2021-04-21] Version 1.14.0
---------------------------
**Library - Feature**
- [PR #32](https://github.com/twilio/twilio-oai/pull/32): add baseUrls to the top-level documents. Thanks to [@childish-sambino](https://github.com/childish-sambino)!

**Library - Fix**
- [PR #31](https://github.com/twilio/twilio-oai/pull/31): format for date type should be 'date' and not 'date-time'. Thanks to [@shwetha-manvinkurke](https://github.com/shwetha-manvinkurke)!

**Api**
- Revert Update the conference participant create `from` and `to` param to be endpoint type for supporting client identifier and sip address
- Update the conference participant create `from` and `to` param to be endpoint type for supporting client identifier and sip address

**Bulkexports**
- moving enum to doc root for auto generating documentation
- adding status enum and default output properties

**Events**
- Change schema_versions prop and key to versions **(breaking change)**

**Messaging**
- Add `use_inbound_webhook_on_number` field in Service API for fetch, create, update, read

**Taskrouter**
- Add `If-Match` Header based on ETag for Task Delete

**Verify**
- Add `AuthPayload` parameter to support verifying a `Challenge` upon creation. This is only supported for `totp` factors.
- Add support to resend the notifications of a `Challenge`. This is only supported for `push` factors.


[2021-04-07] Version 1.13.0
---------------------------
**Api**
- Added `announcement` event to conference status callback events
- Removed optional property `time_limit` in the call create request. **(breaking change)**

**Messaging**
- Add rate_limits field to Messaging Services US App To Person API
- Add usecase field in Service API for fetch, create, update, read
- Add us app to person api and us app to person usecase api as dependents in service
- Add us_app_to_person_registered field in service api for fetch, read, create, update
- Add us app to person api
- Add us app to person usecase api
- Add A2P external campaign api
- Add Usecases API

**Supersim**
- Add Create endpoint to Sims resource

**Verify**
- The `Binding` field is now returned when creating a `Factor`. This value won't be returned for other endpoints.

**Video**
- [Rooms] max_concurrent_published_tracks has got GA maturity


[2021-03-24] Version 1.12.0
---------------------------
**Api**
- Added optional parameter `CallToken` for create calls api
- Add optional property `time_limit` in the call create request.

**Bulkexports**
- adding two new fields with job api queue_position and estimated_completion_time

**Events**
- Add new endpoints to manage subscribed_events in subscriptions

**Numbers**
- Remove feature flags for RegulatoryCompliance endpoints

**Supersim**
- Add SmsCommands resource
- Add fields `SmsCommandsUrl`, `SmsCommandsMethod` and `SmsCommandsEnabled` to a Fleet resource

**Taskrouter**
- Add `If-Match` Header based on ETag for Task Update
- Add `ETag` as Response Headers to Tasks and Reservations

**Video**
- Recording rule beta flag **(breaking change)**
- [Rooms] Add RecordingRules param to Rooms


[2021-03-15] Version 1.11.0
---------------------------
**Library - Feature**
- [PR #30](https://github.com/twilio/twilio-oai/pull/30): add property descriptions to OAI. Thanks to [@JenniferMah](https://github.com/JenniferMah)!

**Library - Chore**
- [PR #29](https://github.com/twilio/twilio-oai/pull/29): add spectral linting to TravisCI build. Thanks to [@eshanholtz](https://github.com/eshanholtz)!

**Events**
- Set maturity to beta

**Messaging**
- Adjust A2P brand registration status enum **(breaking change)**

**Studio**
- Remove internal safeguards for Studio V2 API usage now that it's GA

**Verify**
- Add support for creating and verifying totp factors. Support for totp factors is behind the `api.verify.totp` beta feature.


[2021-02-24] Version 1.10.0
---------------------------
**Library - Fix**
- [PR #27](https://github.com/twilio/twilio-oai/pull/27): add support for null response fields. Thanks to [@eshanholtz](https://github.com/eshanholtz)!
- [PR #26](https://github.com/twilio/twilio-oai/pull/26): remove duplicate enum values. Thanks to [@eshanholtz](https://github.com/eshanholtz)!

**Events**
- Update description of types in the create sink resource

**Messaging**
- Add WA template header and footer
- Remove A2P campaign and use cases API **(breaking change)**
- Add number_registration_status field to read and fetch campaign responses

**Trusthub**
- Make all resources public

**Verify**
- Verify List Attempts API endpoints added.


[2021-02-10] Version 1.9.0
--------------------------
**Library - Feature**
- [PR #19](https://github.com/twilio/twilio-oai/pull/19): add custom types to global schema. Thanks to [@eshanholtz](https://github.com/eshanholtz)!
- [PR #24](https://github.com/twilio/twilio-oai/pull/24): add inline schema titles. Thanks to [@thinkingserious](https://github.com/thinkingserious)!

**Api**
- Revert change that conference participant create `from` and `to` param to be endpoint type for supporting client identifier and sip address
- Update the conference participant create `from` and `to` param to be endpoint type for supporting client identifier and sip address

**Events**
- Documentation should state that no fields are PII

**Flex**
- Adding `notifications` and `markdown` to Flex Configuration

**Messaging**
- Add A2P use cases API
- Add Brand Registrations API
- Add Campaigns API

**Serverless**
- Add runtime field to Build response and as an optional parameter to the Build create endpoint.
- Add @twilio/runtime-handler dependency to Build response example.

**Sync**
- Remove If-Match header for Document **(breaking change)**


[2021-01-27] Version 1.8.0
--------------------------
**Library - Feature**
- [PR #20](https://github.com/twilio/twilio-oai/pull/20): Remove Postman File. Thanks to [@garethpaul](https://github.com/garethpaul)!

**Studio**
- Studio V2 API is now GA

**Supersim**
- Allow updating `CommandsUrl` and `CommandsMethod` on a Fleet


[2021-01-13] Version 1.7.0
--------------------------
**Library - Chore**
- [PR #18](https://github.com/twilio/twilio-oai/pull/18): add ahoy msg. Thanks to [@garethpaul](https://github.com/garethpaul)!

**Library - Fix**
- [PR #17](https://github.com/twilio/twilio-oai/pull/17): making specs conform with the OpenAPI specification. Thanks to [@shwetha-manvinkurke](https://github.com/shwetha-manvinkurke)!

**Api**
- Add 'Electric Imp v1 Usage' to usage categories

**Conversations**
- Changed `last_read_message_index` type in Participant's resource **(breaking change)**

**Insights**
- Added `created_time` to call summary.

**Sync**
- Remove HideExpired query parameter for filtering Sync Documents with expired **(breaking change)**

**Video**
- [Rooms] Expose maxConcurrentPublishedTracks property in Room resource


[2020-12-16] Version 1.6.0
--------------------------
**Library - Feature**
- [PR #16](https://github.com/twilio/twilio-oai/pull/16): add operation IDs. Thanks to [@JenniferMah](https://github.com/JenniferMah)!

**Api**
- Updated `call_event` default_output_properties to request and response.

**Conversations**
- Added `last_read_message_index` and `last_read_timestamp` to Participant's resource update operation
- Added `is_notifiable` and `is_online` to User's resource
- Added `reachability_enabled` parameters to update method for Conversation Service Configuration resource

**Messaging**
- Added WA template quick reply, URL, and phone number buttons


[2020-12-08] Version 1.5.0
--------------------------
**Library - Chore**
- [PR #14](https://github.com/twilio/twilio-oai/pull/14): replace tags with vendor extension. Thanks to [@thinkingserious](https://github.com/thinkingserious)!

**Library - Fix**
- [PR #11](https://github.com/twilio/twilio-oai/pull/11): fixing semantic errors in the specs. Thanks to [@shwetha-manvinkurke](https://github.com/shwetha-manvinkurke)!

**Api**
- Added optional `RecordingTrack` parameter for create calls, create participants, and create call recordings
- Removed deprecated Programmable Chat usage record categories **(breaking change)**


[2020-12-02] Version 1.4.0
--------------------------
**Library - Feature**
- [PR #8](https://github.com/twilio/twilio-oai/pull/8): Splitting up openAPI specs by version. Thanks to [@shwetha-manvinkurke](https://github.com/shwetha-manvinkurke)!

**Api**
- Remove `RecordingTrack` parameter for create calls, create participants, and create call recordings **(breaking change)**
- Added `RecordingTrack` parameter for create calls and create call recordings
- Add optional property `recording_track` in the participant create request

**Lookups**
- Changed `caller_name` and `carrier` properties type to object **(breaking change)**

**Trunking**
- Added dual channel recording options for Trunks.


[2020-11-18] Version 1.3.0
--------------------------
**Api**
- Add new call events resource - GET /2010-04-01/Accounts/{account_sid}/Calls/{call_sid}/Events.json

**Conversations**
- Fixed default response property issue for Service Notifications Configuration

**Insights**
- Removing call_sid from participant summary. **(breaking change)**

**Serverless**
- Allow Service unique name to be used in path (in place of SID) in Service update request

**Sync**
- Added HideExpired query parameter for filtering Sync Documents with expired

**Verify**
- Challenge `Details` and `HiddenDetails` properties are now marked as `PII`
- Challenge `expiration_date` attribute updated to set a default value of five (5) minutes and to allow max dates of one (1) hour after creation.
- Entity `identity` attribute updated to allow values between 8 and 64 characters.
- Verify Service frinedly_name attribute updated from 64 max lenght to 30 characters.


[2020-11-05] Version 1.2.0
--------------------------
**Api**
- Added `verify-push` to `usage_record` API

**Bulkexports**
- When creating a custom export the StartDay, EndDay, and FriendlyName fields were required but this was not reflected in the API documentation.  The API itself failed the request without these fields. **(breaking change)**
- Added property descriptions for Custom Export create method
- Clarified WebhookUrl and WebhookMethod must be provided together for Custom Export

**Insights**
- Added video room and participant summary apis.

**Ip_messaging**
- Create separate definition for ip-messaging
- Restore v2 endpoints for ip-messaging

**Verify**
- Verify Push madurity were updated from `preview` to `beta`
- `twilio_sandbox_mode` header was removed from Verify Push resources **(breaking change)**

**Video**
- [Rooms] Add Recording Rules API


[2020-10-14] Version 1.1.0
--------------------------
**Ai**
- Add `Annotation Project` and `Annotation Task` endpoints
- Add `Primitives` endpoints
- Add `meta.total` to the search endpoint

**Conversations**
- Mutable Conversation Unique Names

**Insights**
- Added `trust` to summary.

**Preview**
- Simplified `Channels` resource. The path is now `/BrandedChannels/branded_channel_sid/Channels` **(breaking change)**

**Verify**
- Changed parameters (`config` and `binding`) to use dot notation instead of JSON string (e.i. Before: `binding={"alg":"ES256", "public_key": "xxx..."}`, Now: `Binding.Alg="ES256"`, `Binding.PublicKey="xxx..."`). **(breaking change)**
- Changed parameters (`details` and `hidden_details`) to use dot notation instead of JSON string (e.i. Before: `details={"message":"Test message", "fields": "[{\"label\": \"Action 1\", \"value\":\"value 1\"}]"}`, Now: `details.Message="Test message"`, `Details.Fields=["{\"label\": \"Action 1\", \"value\":\"value 1\"}"]`). **(breaking change)**
- Removed `notify_service_sid` from `push` service configuration object. Add `Push.IncludeDate`, `Push.ApnCredentialSid` and `Push.FcmCredentialSid` service configuration parameters. **(breaking change)**


[2020-09-28] Version 1.0.1
--------------------------
**Api**
- Add optional property `call_reason` in the participant create request
- Make sip-domain-service endpoints available in stage-au1 and prod-au1

**Messaging**
- Removed beta feature gate from WhatsApp Templates API

**Serverless**
- Add Build Status endpoint

**Video**
- [Rooms] Add new room type "go" for WebRTC Go


[2020-09-21] Version 1.0.0
--------------------------
**Library - Docs**
- [PR #4](https://github.com/twilio/twilio-oai/pull/4): Adding README.md. Thanks to [@garethpaul](https://github.com/garethpaul)!

**Accounts**
- Add Auth Token rotation API

**Conversations**
- Change resource path for Webhook Configuration

**Events**
- Schemas API get all Schemas names and versions


[2020-09-17] Version 0.1.1
--------------------------
**Conversations**
- Expose Configuration and Service Configuration resources
- Add Unique Name support for Conversations
- Add Services Push Notification resource
- Add Service scoped Conversation resources
- Support Identity in Users resource endpoint

**Messaging**
- GA Deactivation List API
- Add domain cert API's(fetch, update, create) for link tracker

**Numbers**
- Add API endpoint for Supporting Document deletion

**Proxy**
- Updated usage of FailOnParticipantConflict param to apply only to accounts with ProxyAllowParticipantConflict account flag

**Supersim**
- Add `AccountSid` parameter to Sim resource update request
- Add `ready` status as an available status for a Sim resource


[2020-08-26] Version 0.1.0
--------------------------
