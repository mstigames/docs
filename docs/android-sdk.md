## Android payment sdk

Android payment SDK allows to easily add MSTI payments powered by Stripe to a unity project. 

### Requirements

- Unity 2022 and above
- Android 7.0 (API level)


## Getting stared
### 1. Import the SDK into Unity
### 2. Resolve android dependenceis
1. Enable custom gradle Template
2. If you use [EDM4U](https://github.com/googlesamples/unity-jar-resolver) android dependenceis will be automatically added to your project, otherwise copy packages from `/msti/Editor/dependencies.xml` to `mainTemplate.gradle`

## Unity IAP integration

The SDK works both with codeless and coded Unity IAP 
integrations. 

### Codless payments
Initialise MSTI payments
```csharp
MSTI.Payments.Initialize();
```
It's critical to make this call before any Unity Codeless components are initialised. You'll receive a warning in case MSTI initialize has been called too late.

### Coded payments
Add `MstiPaymentsModule` to your store `ConfigurationBuilder`
```
var builder = ConfigurationBuilder.Instance (MstiPaymentsModule.Instance(), StandardPurchasingModule.Instance ());
```

## Manual integartion
If you don't use Unity IAP please email support@msti.games with brief explanation of your existing payment implementation we'll send you bespoke guide for integrating our SDK manually.

