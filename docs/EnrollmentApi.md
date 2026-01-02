# CyberSource::EnrollmentApi

All URIs are relative to *https://apitest.cybersource.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**enroll_card**](EnrollmentApi.md#enroll_card) | **POST** /acp/v1/tokens | Enroll a card


# **enroll_card**
> AgenticCardEnrollmentResponse200 enroll_card(agentic_card_enrollment_request)

Enroll a card

Enroll a card for tokenization during the customer's account registration or when the customer starts a new purchase intent.

### Example
```ruby
# load the gem
require 'cybersource_rest_client'

api_instance = CyberSource::EnrollmentApi.new

agentic_card_enrollment_request = CyberSource::AgenticCardEnrollmentRequest.new # AgenticCardEnrollmentRequest | 


begin
  #Enroll a card
  result = api_instance.enroll_card(agentic_card_enrollment_request)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling EnrollmentApi->enroll_card: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agentic_card_enrollment_request** | [**AgenticCardEnrollmentRequest**](AgenticCardEnrollmentRequest.md)|  | 

### Return type

[**AgenticCardEnrollmentResponse200**](AgenticCardEnrollmentResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json;charset=utf-8
 - **Accept**: application/hal+json;charset=utf-8



