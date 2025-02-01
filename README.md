# Expo AsyncStorage Initialization Error

This repository demonstrates a common error encountered when using AsyncStorage in Expo applications. The problem arises from attempting to access AsyncStorage before it's fully initialized during the app's startup sequence.  This typically leads to undefined behavior or errors indicating AsyncStorage is unavailable.

The `bug.js` file showcases the erroneous code. The `bugSolution.js` file provides a corrected version, utilizing the `AsyncStorage.ready` method to ensure the module is initialized before interacting with it.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary packages.
3. Run the application using Expo Go or a similar method.
4. Observe the error message in the console, noting that the initial attempt to read from AsyncStorage fails.
5. Uncomment the corrected code in `bugSolution.js` to see the issue resolved.

## Solution

The provided solution introduces a simple check using AsyncStorage.ready. This method ensures that AsyncStorage is fully initialized before any access attempts. This prevents the error and guarantees proper operation.