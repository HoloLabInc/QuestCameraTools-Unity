# QuestCameraTools-Unity

**QuestCameraTools-Unity** is a Unity library that leverages the Meta Quest Passthrough Camera API to perform spatial alignment using QR codes or Immersal.

## Requirements

For hardware and device prerequisites, please refer to the official samples and documentation:

- https://github.com/oculus-samples/Unity-PassthroughCameraApiSamples#hardware
- https://developers.meta.com/horizon/documentation/unity/unity-pca-overview/#general-prerequisites

## QR Code Tracking

https://github.com/user-attachments/assets/0fae755e-6ca2-4a43-9bee-024cf7dc3feb

### Sample Project

The Unity project located in [unity/QRTracking-6000](./unity/QRTracking-6000/) is the sample project for QR Code Tracking.

- `Assets/App/Scenes/ArbitraryQRTrackingSample.scene` demonstrates how to track any QR code that comes into view.
- `Assets/App/Scenes/SpecificQRTrackingSample.scene` demonstrates how to track specific, predefined QR codes (identified by the strings embedded in each code).

### Importing the UPM Packages into Your Project

Use Unity 6000.0 or later.

Beforehand, import the `com.meta.xr.sdk.core` and `com.meta.xr.mrutilitykit` packages.

Also, make sure the Depth API is enabled. Please refer to the following page:  
https://developers.meta.com/horizon/documentation/unity/unity-depthapi-overview/#requirements

Open `Packages\manifest.json` and add the following lines in "dependencies":

```json
"jp.co.hololab.questcameratools.core": "https://github.com/HoloLabInc/QuestCameraTools-Unity.git?path=packages/jp.co.hololab.questcameratools.core",
"jp.co.hololab.questcameratools.qr": "https://github.com/HoloLabInc/QuestCameraTools-Unity.git?path=packages/jp.co.hololab.questcameratools.qr",
"jp.co.hololab.questcameratools.qr.libraries": "https://github.com/HoloLabInc/QuestCameraTools-Unity.git?path=packages/jp.co.hololab.questcameratools.qr.libraries",
```

For usage, please refer to the sample scene in the sample project.

## Localization with Immersal

https://github.com/user-attachments/assets/b14f3860-15fc-4936-8c8d-b9eed0a777b2

### Sample Project

The Unity project located in [unity/LocalizationWithImmersal-6000](./unity/LocalizationWithImmersal-6000/) is the sample project for Immersal localization.

`Assets/App/Scenes/SimpleLocalizationSample.scene` is the sample scene.
In this scene, assign your Immersal Developer Token to the `ImmersalSDKForQuest` object in the scene.
Configure the map on the `XR Map` object, which is a child of `XRSpace`.

For detailed instructions on using Immersal, see the official documentation:  
https://developers.immersal.com/docs/unitysdk/samplescenes/

### Importing the UPM Packages into Your Project

Use Unity 6000.0 or later.

First, import the `com.meta.xr.sdk.core` package.

Next, add the Immersal SDK by following the installation guide here:  
https://developers.immersal.com/docs/unitysdk/tutorial/#installation

Open `Packages\manifest.json` and add the following lines in "dependencies":

```json
"jp.co.hololab.questcameratools.core": "https://github.com/HoloLabInc/QuestCameraTools-Unity.git?path=packages/jp.co.hololab.questcameratools.core",
"jp.co.hololab.questcameratools.immersal": "https://github.com/HoloLabInc/QuestCameraTools-Unity.git?path=packages/jp.co.hololab.questcameratools.immersal",
```

For usage, please refer to the sample scene in the sample project.

## About Trademarks

QR Code is registered trademark of DENSO WAVE INCORPORATED.
