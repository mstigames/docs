## Android payment sdk

Android payment SDK allows to easily add MSTI payments powered by Stripe to a unity project. 

### Requirements

- Unity 2022 or later
- Android 7.0 (API level) or higher


## Getting stared
#### 1. Import the SDK into Unity
#### 2. Resolve android dependenceis
1. Enable custom gradle Template, properties and settings in `Player Settings > Publishing Settings` 
2. If you use [EDM4U](https://github.com/googlesamples/unity-jar-resolver), Android dependenceis will be automatically added to your project, otherwise copy packages from `/msti/Editor/dependencies.xml` to `mainTemplate.gradle`

## Unity IAP integration

The SDK supports both codeless and coded Unity IAP integrations.

### Codless payments
Initialize MSTI payments with the following code:
```csharp
MSTI.Payments.Initialize();
```
Ensure this call is made before any Unity Codeless components are initialized. If MSTI initialization is called too late, a warning will be displayed.

### Coded payments
Add `MstiPaymentsModule` to your store's `ConfigurationBuilder`
```
var builder = ConfigurationBuilder.Instance (MstiPaymentsModule.Instance(), StandardPurchasingModule.Instance ());
```

## Manual integartion
If you don't use Unity IAP please email [support@msti.games](mailto:support@msti.games) with a brief explanation of your existing payment implementation. We will provide a bespoke guide for integrating our SDK manually.