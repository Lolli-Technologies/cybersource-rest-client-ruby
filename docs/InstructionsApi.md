# CyberSource::InstructionsApi

All URIs are relative to *https://apitest.cybersource.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_purchase_intent**](InstructionsApi.md#cancel_purchase_intent) | **PUT** /acp/v1/instructions/{instructionId}/cancel | Cancel a purchase intent
[**confirm_transaction_events**](InstructionsApi.md#confirm_transaction_events) | **POST** /acp/v1/instructions/{instructionId}/confirmations | Confirm transaction events
[**initiate_purchase_intent**](InstructionsApi.md#initiate_purchase_intent) | **POST** /acp/v1/instructions | Initiate a purchase intent
[**retrieve_payment_credentials**](InstructionsApi.md#retrieve_payment_credentials) | **POST** /acp/v1/instructions/{instructionId}/credentials | Retrieve payment credentials
[**update_purchase_intent**](InstructionsApi.md#update_purchase_intent) | **PUT** /acp/v1/instructions/{instructionId} | Update a purchase intent


# **cancel_purchase_intent**
> AgenticCreatePurchaseIntentResponse200 cancel_purchase_intent(instruction_id, agentic_cancel_purchase_intent_request)

Cancel a purchase intent

Cancels an existing purchase intent identified by the transaction ID.

### Example
```ruby
# load the gem
require 'cybersource_rest_client'

api_instance = CyberSource::InstructionsApi.new

instruction_id = 'instruction_id_example' # String | 

agentic_cancel_purchase_intent_request = CyberSource::AgenticCancelPurchaseIntentRequest.new # AgenticCancelPurchaseIntentRequest | Unique identifier for the purchase intent instruction.


begin
  #Cancel a purchase intent
  result = api_instance.cancel_purchase_intent(instruction_id, agentic_cancel_purchase_intent_request)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling InstructionsApi->cancel_purchase_intent: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **instruction_id** | **String**|  | 
 **agentic_cancel_purchase_intent_request** | [**AgenticCancelPurchaseIntentRequest**](AgenticCancelPurchaseIntentRequest.md)| Unique identifier for the purchase intent instruction. | 

### Return type

[**AgenticCreatePurchaseIntentResponse200**](AgenticCreatePurchaseIntentResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=utf-8
 - **Accept**: application/hal+json;charset=utf-8



# **confirm_transaction_events**
> AgenticConfirmTransactionEventsResponse202 confirm_transaction_events(instruction_id, agentic_confirm_transaction_events_request)

Confirm transaction events

Agents send the confirm transaction events to notify the payment processing is done

### Example
```ruby
# load the gem
require 'cybersource_rest_client'

api_instance = CyberSource::InstructionsApi.new

instruction_id = 'instruction_id_example' # String | Unique identifier for the purchase intent instruction.

agentic_confirm_transaction_events_request = CyberSource::AgenticConfirmTransactionEventsRequest.new # AgenticConfirmTransactionEventsRequest | 


begin
  #Confirm transaction events
  result = api_instance.confirm_transaction_events(instruction_id, agentic_confirm_transaction_events_request)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling InstructionsApi->confirm_transaction_events: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **instruction_id** | **String**| Unique identifier for the purchase intent instruction. | 
 **agentic_confirm_transaction_events_request** | [**AgenticConfirmTransactionEventsRequest**](AgenticConfirmTransactionEventsRequest.md)|  | 

### Return type

[**AgenticConfirmTransactionEventsResponse202**](AgenticConfirmTransactionEventsResponse202.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=utf-8
 - **Accept**: application/hal+json;charset=utf-8



# **initiate_purchase_intent**
> AgenticCreatePurchaseIntentResponse200 initiate_purchase_intent(agentic_create_purchase_intent_request)

Initiate a purchase intent

Creates a new purchase intent with the provided details.

### Example
```ruby
# load the gem
require 'cybersource_rest_client'

api_instance = CyberSource::InstructionsApi.new

agentic_create_purchase_intent_request = CyberSource::AgenticCreatePurchaseIntentRequest.new # AgenticCreatePurchaseIntentRequest | 


begin
  #Initiate a purchase intent
  result = api_instance.initiate_purchase_intent(agentic_create_purchase_intent_request)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling InstructionsApi->initiate_purchase_intent: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agentic_create_purchase_intent_request** | [**AgenticCreatePurchaseIntentRequest**](AgenticCreatePurchaseIntentRequest.md)|  | 

### Return type

[**AgenticCreatePurchaseIntentResponse200**](AgenticCreatePurchaseIntentResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=utf-8
 - **Accept**: application/hal+json;charset=utf-8



# **retrieve_payment_credentials**
> AgenticRetrievePaymentCredentialsResponse200 retrieve_payment_credentials(instruction_id, agentic_retrieve_payment_credentials_request)

Retrieve payment credentials

Retrieve a customer's tokenized payment credentials to complete the transaction.

### Example
```ruby
# load the gem
require 'cybersource_rest_client'

api_instance = CyberSource::InstructionsApi.new

instruction_id = 'instruction_id_example' # String | Unique identifier for the purchase intent instruction.

agentic_retrieve_payment_credentials_request = CyberSource::AgenticRetrievePaymentCredentialsRequest.new # AgenticRetrievePaymentCredentialsRequest | 


begin
  #Retrieve payment credentials
  result = api_instance.retrieve_payment_credentials(instruction_id, agentic_retrieve_payment_credentials_request)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling InstructionsApi->retrieve_payment_credentials: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **instruction_id** | **String**| Unique identifier for the purchase intent instruction. | 
 **agentic_retrieve_payment_credentials_request** | [**AgenticRetrievePaymentCredentialsRequest**](AgenticRetrievePaymentCredentialsRequest.md)|  | 

### Return type

[**AgenticRetrievePaymentCredentialsResponse200**](AgenticRetrievePaymentCredentialsResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=utf-8
 - **Accept**: application/hal+json;charset=utf-8



# **update_purchase_intent**
> AgenticCreatePurchaseIntentResponse200 update_purchase_intent(instruction_id, agentic_update_purchase_intent_request)

Update a purchase intent

Updates an existing purchase intent identified by the transaction ID.

### Example
```ruby
# load the gem
require 'cybersource_rest_client'

api_instance = CyberSource::InstructionsApi.new

instruction_id = 'instruction_id_example' # String | Unique identifier for the purchase intent instruction.

agentic_update_purchase_intent_request = CyberSource::AgenticUpdatePurchaseIntentRequest.new # AgenticUpdatePurchaseIntentRequest | 


begin
  #Update a purchase intent
  result = api_instance.update_purchase_intent(instruction_id, agentic_update_purchase_intent_request)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling InstructionsApi->update_purchase_intent: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **instruction_id** | **String**| Unique identifier for the purchase intent instruction. | 
 **agentic_update_purchase_intent_request** | [**AgenticUpdatePurchaseIntentRequest**](AgenticUpdatePurchaseIntentRequest.md)|  | 

### Return type

[**AgenticCreatePurchaseIntentResponse200**](AgenticCreatePurchaseIntentResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=utf-8
 - **Accept**: application/hal+json;charset=utf-8



