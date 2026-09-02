# AuthAPI

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**acceptInvite**](AuthAPI.md#acceptinvite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
[**forgotPassword**](AuthAPI.md#forgotpassword) | **POST** /auth/forgot-password | Send a password reset email to the user
[**login**](AuthAPI.md#login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP)
[**logout**](AuthAPI.md#logout) | **POST** /auth/logout | Log out the current user (kills the assay session)
[**magicLinkLogin**](AuthAPI.md#magiclinklogin) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link)
[**magicLinkVerify**](AuthAPI.md#magiclinkverify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in
[**register**](AuthAPI.md#register) | **POST** /auth/register | Register a new user account
[**resetPassword**](AuthAPI.md#resetpassword) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token
[**totpEnable**](AuthAPI.md#totpenable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code
[**totpSetup**](AuthAPI.md#totpsetup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes)
[**verifyEmail**](AuthAPI.md#verifyemail) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token


# **acceptInvite**
```swift
    open class func acceptInvite(acceptInviteRequest: AcceptInviteRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let acceptInviteRequest = AcceptInviteRequest(firstName: "firstName_example", lastName: "lastName_example", password: "password_example", privacyAccepted: false, token: "token_example") // AcceptInviteRequest | 

// Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
AuthAPI.acceptInvite(acceptInviteRequest: acceptInviteRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **acceptInviteRequest** | [**AcceptInviteRequest**](AcceptInviteRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **forgotPassword**
```swift
    open class func forgotPassword(forgotPasswordRequest: ForgotPasswordRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Send a password reset email to the user

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let forgotPasswordRequest = ForgotPasswordRequest(email: "email_example") // ForgotPasswordRequest | 

// Send a password reset email to the user
AuthAPI.forgotPassword(forgotPasswordRequest: forgotPasswordRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **forgotPasswordRequest** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login**
```swift
    open class func login(loginRequest: LoginRequest, completion: @escaping (_ data: AuthResponse?, _ error: Error?) -> Void)
```

Authenticate a user with email + password (optional TOTP)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let loginRequest = LoginRequest(email: "email_example", password: "password_example", totpCode: "totpCode_example") // LoginRequest | 

// Authenticate a user with email + password (optional TOTP)
AuthAPI.login(loginRequest: loginRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **loginRequest** | [**LoginRequest**](LoginRequest.md) |  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **logout**
```swift
    open class func logout(completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Log out the current user (kills the assay session)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Log out the current user (kills the assay session)
AuthAPI.logout() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **magicLinkLogin**
```swift
    open class func magicLinkLogin(magicLinkRequest: MagicLinkRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Request a magic link login (sends an email with a one-time link)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let magicLinkRequest = MagicLinkRequest(email: "email_example") // MagicLinkRequest | 

// Request a magic link login (sends an email with a one-time link)
AuthAPI.magicLinkLogin(magicLinkRequest: magicLinkRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **magicLinkRequest** | [**MagicLinkRequest**](MagicLinkRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **magicLinkVerify**
```swift
    open class func magicLinkVerify(magicLinkVerifyRequest: MagicLinkVerifyRequest, completion: @escaping (_ data: AuthResponse?, _ error: Error?) -> Void)
```

Verify a magic link token and log the user in

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let magicLinkVerifyRequest = MagicLinkVerifyRequest(token: "token_example") // MagicLinkVerifyRequest | 

// Verify a magic link token and log the user in
AuthAPI.magicLinkVerify(magicLinkVerifyRequest: magicLinkVerifyRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **magicLinkVerifyRequest** | [**MagicLinkVerifyRequest**](MagicLinkVerifyRequest.md) |  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register**
```swift
    open class func register(registerRequest: RegisterRequest, completion: @escaping (_ data: AuthResponse?, _ error: Error?) -> Void)
```

Register a new user account

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let registerRequest = RegisterRequest(companyName: "companyName_example", email: "email_example", firstName: "firstName_example", lastName: "lastName_example", password: "password_example", privacyAccepted: false) // RegisterRequest | 

// Register a new user account
AuthAPI.register(registerRequest: registerRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **registerRequest** | [**RegisterRequest**](RegisterRequest.md) |  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resetPassword**
```swift
    open class func resetPassword(resetPasswordRequest: ResetPasswordRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Reset the user's password using a reset token

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let resetPasswordRequest = ResetPasswordRequest(newPassword: "newPassword_example", token: "token_example") // ResetPasswordRequest | 

// Reset the user's password using a reset token
AuthAPI.resetPassword(resetPasswordRequest: resetPasswordRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resetPasswordRequest** | [**ResetPasswordRequest**](ResetPasswordRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **totpEnable**
```swift
    open class func totpEnable(totpEnableRequest: TotpEnableRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Enable TOTP two-factor authentication by verifying a code

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let totpEnableRequest = TotpEnableRequest(code: "code_example") // TotpEnableRequest | 

// Enable TOTP two-factor authentication by verifying a code
AuthAPI.totpEnable(totpEnableRequest: totpEnableRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **totpEnableRequest** | [**TotpEnableRequest**](TotpEnableRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **totpSetup**
```swift
    open class func totpSetup(completion: @escaping (_ data: TotpSetupResponse?, _ error: Error?) -> Void)
```

Set up TOTP two-factor authentication (generates secret + backup codes)

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI


// Set up TOTP two-factor authentication (generates secret + backup codes)
AuthAPI.totpSetup() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TotpSetupResponse**](TotpSetupResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verifyEmail**
```swift
    open class func verifyEmail(verifyEmailRequest: VerifyEmailRequest, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Verify a user's email address using a verification token

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import SimpleBillyAPI

let verifyEmailRequest = VerifyEmailRequest(token: "token_example") // VerifyEmailRequest | 

// Verify a user's email address using a verification token
AuthAPI.verifyEmail(verifyEmailRequest: verifyEmailRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verifyEmailRequest** | [**VerifyEmailRequest**](VerifyEmailRequest.md) |  | 

### Return type

Void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

