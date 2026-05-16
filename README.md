# BoltEarthUiSdkCore

BoltEarth Android SDK for EV charging integrations.

## Installation

ruby pod 'BoltEarthUiSdkCore',     :podspec => 'https://raw.githubusercontent.com/debashish310/BoltEarthUiSdkCore/main/BoltEarthUiSdkCore.podspec' 

## Access Requirement

The BoltEarth SDK is intended only for approved and authorized applications.

Before integrating the SDK, your application must be configured and whitelisted by the Bolt.Earth team. The SDK internally reads the host application's Bundle Identifier and uses it for backend validation and API authorization.

If the application's Bundle Identifier is not configured in Bolt.Earth backend systems, certain SDK APIs and flows may fail to function correctly.

Please contact the Bolt.Earth team before integration and share the following details:

- Android Bundle Identifier  
  Example: com.company.app

## Requirements

- Android minSDK - 26
