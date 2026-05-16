# BoltEarthUiSdkCore

BoltEarth Android SDK for EV charging integrations.

## Installation
settings.gradle

dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        maven {
            url = uri("https://maven.juspay.in/jp-build-packages/hyper-sdk/")
        }
        maven {
            url = uri("https://jitpack.io")
            content {
                excludeGroup("io.github.boltearth") // keep JitPack away from bolt-earth
            }
        }
        maven {
            url = uri("https://raw.githubusercontent.com/BOLT-EARTH/bolt-earth-android-sdk/main/releases")
            // no content filter — let it resolve freely
        }
    }
}


build.gradle(app) 

implementation("io.github.boltearth:bolt-earth-ui-sdk:1.0.0")

also need to install and define @HiltAndroidApp entry point for the application instance.

## Access Requirement

The BoltEarth SDK is intended only for approved and authorized applications.

Before integrating the SDK, your application must be configured and whitelisted by the Bolt.Earth team. The SDK internally reads the host application's Bundle Identifier and uses it for backend validation and API authorization.

If the application's Bundle Identifier is not configured in Bolt.Earth backend systems, certain SDK APIs and flows may fail to function correctly.

Please contact the Bolt.Earth team before integration and share the following details:

- Android Bundle Identifier  
  Example: com.company.app

## Requirements

- Android minSDK - 26
