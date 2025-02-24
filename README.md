# Expo Linking.getInitialURL() Android Bug

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API on Android. The promise sometimes resolves to `null` even when a deep link is opened, leading to unexpected behavior. This is inconsistent with iOS behavior.

## Bug Reproduction

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Open a deep link (e.g., `myapp://somepath`).
4. Observe that `Linking.getInitialURL()` sometimes resolves to `null` despite the deep link being opened.

## Potential Causes

* Timing issues in the Android Linking API.
* Conflicts with other libraries or system processes.
* Expo's internal handling of deep links.

## Solution

A robust solution requires handling potential `null` values from `Linking.getInitialURL()` and implementing appropriate fallback mechanisms.