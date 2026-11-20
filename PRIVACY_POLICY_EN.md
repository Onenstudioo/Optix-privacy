# Optix Privacy Policy

**Last updated:** 20 November 2026  
**App version:** 1.4.3  
**Developer:** OnenStudioo  
**Contact:** onenstudioo@gmail.com

Optix is an Android privacy helper that uses the front camera to alert you when more than one face is present in the camera view. Optix counts faces; it does not recognize or identify people, perform biometric authentication, measure eye movement, or determine whether someone is looking at your screen. A detection is not proof that another person can see your screen, and detections may be inaccurate or incomplete.

## 1. At a glance

- Optix analyzes camera frames on your device. It does not record them as photos or videos, upload them to its own servers, or share them.
- Optix has no account system, advertising, user profiling, or first-party analytics/tracking system.
- Optix does not request location, microphone, contacts, or file/storage access.
- Statistics and app preferences are stored locally in app-specific storage.
- Camera protection is started by the user. It does not start automatically when the phone boots or the app opens.

## 2. Camera and face detection

Camera permission is used to capture images from the front camera and count faces. When protection is started, the camera may run through a camera-type Android foreground service with the system camera indicator and Optix's ongoing notification visible, allowing protection to continue while you switch apps. You can stop protection from the app or its notification.

Frames are processed on-device, in memory for the time needed for analysis, using CameraX and Google ML Kit face detection. Optix does not save frames to files, create or store face images/templates/identities, or transmit camera frames to its own server. When the phone is locked, camera protection is suspended and the camera is released. Analysis may stop if camera permission is revoked, the camera privacy control is off, another app is using the camera, or Android stops the service.

Optix uses face-detection results only for its protection and alert logic. Detection is not guaranteed: distant, partially visible, moving, poorly lit, or non-frontal faces may be missed. An alert cannot conclusively establish that someone is viewing your screen or that privacy has been compromised.

## 3. Adaptive scanning

When adaptive scanning is enabled, Optix may adjust the analysis frequency on-device based on the current face count. Optix does not read battery state for this decision. The current face count is used in the analysis process and is not stored to create a face profile or sent by Optix.

## 4. Information stored on the device

Optix may store the following limited information for its local Statistics feature:

- total and daily counts of second-face alerts,
- number of protection sessions and total protection time,
- time of the last alert,
- app preferences (such as language, alert sound and sound toggle, vibration and pattern, detection options, adaptive scanning and travel-suggestion preference),
- if travel suggestions are enabled, that preference and the time the last suggestion was shown.

These records are stored in app-specific local storage and are not sent to Optix servers. Statistics do not include camera frames, face images, face templates, identity information, location, or trip-route history.

**Deletion:** The **Reset statistics** action on the Statistics screen resets statistics; it does not reset app preferences. To remove all local app data, clear Optix's app storage in Android settings or uninstall the app.

## 5. Notifications and Quick Settings

Optix may show an ongoing service notification while protection is active, a second-face alert, and—if travel suggestions are enabled—a suggestion notification. Alert detail may be limited by the alert-visibility preference. Android notification permission and channel settings affect notification behavior.

The Optix Quick Settings tile is a shortcut to start or stop protection. It manages protection state and is not a separate profiling or data-collection feature.

## 6. “Suggest when travelling” (optional)

This feature is off by default. If enabled, Optix uses Google Play services Activity Recognition to detect vehicle-related activity and may request Android's **Physical activity** permission, depending on Android version. A detected vehicle transition is used to show a suggestion notification; Optix does not start protection automatically. Location permission is not requested. Optix does not keep movement, vehicle, or trip history; it may store the feature preference and the time the last suggestion was shown locally. You can disable the feature in Settings and revoke its permission in Android settings. If the feature is enabled, the activity-recognition subscription may be renewed after a device restart or app update; this does not start the camera at boot.

Activity Recognition is provided by Google Play services. Google's handling of data related to that service is subject to Google's policies and disclosures.

## 7. Permissions

Optix may use these Android permissions or capabilities:

- **Camera:** Capture front-camera frames and count faces on-device after you start protection.
- **Notifications:** Show the protection service, alerts, and optional travel suggestions (may require permission on Android 13 and later).
- **Camera foreground service:** Keep camera use visible while protection is active.
- **Vibration:** Provide alert vibration when enabled.
- **Physical activity / Activity Recognition:** Only for the optional “Suggest when travelling” feature.
- **Boot completed receiver:** Renew the Activity Recognition subscription only when “Suggest when travelling” is enabled; it is not used to start the camera.

Optix does not request microphone, location, contacts, or file/storage permissions. Permissions can be revoked in Android settings; the related feature may then be unavailable.

## 8. Third-party components and services

Optix uses **Google ML Kit** for face detection and **Google Play services** for optional activity recognition. Face detection runs on-device. Google SDKs and services may, within their own scope, process technical or diagnostic information to provide their services, measure reliability/performance, or troubleshoot issues. Such processing is outside Optix's control and is governed by Google's policies. Optix is not designed to send camera frames to Google or any other third party.

- Google Privacy Policy: https://policies.google.com/privacy
- ML Kit Android data disclosure: https://developers.google.com/ml-kit/android-data-disclosure

Optix does not include its own advertising network, analytics SDK, account system, server, or data-broker integration.

## 9. Sharing, sale, and security

Optix does not sell user data or profile users for advertising. Optix does not transfer its local statistics or preferences to third parties. Optix does not transmit camera data over the network. Local data is held within Android app storage isolation; however, no absolute security guarantee can be made against device access, operating-system conditions, or third-party system components.

## 10. Retention

Optix does not retain user data on its own servers. Local statistics and preferences may remain on the device until you reset them, clear the app's storage, or uninstall Optix. Resetting statistics does not delete preferences.

## 11. Children's privacy

Optix is not designed specifically for children and is not intended to knowingly collect personal information from children.

## 12. Changes to this policy

This policy may be updated if Optix features, permissions, or data practices change. The current version will be published on this page with an updated date and app version.

## 13. Contact

Privacy questions or requests: **onenstudioo@gmail.com**
