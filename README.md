# React Native Dimensions Inaccuracy on Android

This repository demonstrates a common issue encountered when using the `Dimensions.get('window')` API in React Native on Android. The API may return inaccurate dimensions immediately after launch or following a configuration change, causing layout problems.

## Problem

The `Dimensions` API doesn't always provide up-to-date screen dimensions immediately. This is especially noticeable on Android, often resulting in components rendered with incorrect sizes.

## Solution

The recommended solution is to listen for the `Dimensions.addEventListener` event to ensure you're using the accurate updated values after the initial render. This approach ensures your UI reacts correctly to changes in screen orientation or configuration changes.