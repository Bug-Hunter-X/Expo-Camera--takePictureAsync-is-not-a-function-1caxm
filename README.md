# Expo Camera: takePictureAsync is not a function

This repository demonstrates a common error encountered when using the Expo Camera API: `Camera.takePictureAsync is not a function`. This issue arises from attempting to use `takePictureAsync` before the camera has completely initialized.

## Problem

The `Camera` component requires time to initialize. If you try to call `takePictureAsync` too early, it may result in the error because the function might not yet be available on the `Camera` instance.

## Solution

The solution involves ensuring that `takePictureAsync` is called only after the camera is ready. This is typically achieved using the `onCameraReady` callback provided by the `Camera` component.