# Expo Go iOS Camera Crash

This repository demonstrates a bug in Expo Go on iOS where the Camera component crashes without providing an error message when attempting to take a picture. The issue is specific to iOS devices; Android devices function correctly. The likely cause is the asynchronous nature of the camera permission request and image capture process.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using Expo Go on an iOS device.
4. Attempt to take a picture using the Camera component.
5. Observe the app crash without any visible error message in the Expo Go console.

## Solution

The solution involves a more robust error-handling mechanism and careful management of the asynchronous operations related to camera access and image capture. The solution is provided in `bugSolution.js` and addresses these issues by making sure the camera is actually ready before the taking picture and add proper error handling in promise chains.