# Unhandled FormatException in Dart JSON Decoding

This repository demonstrates a common error in Dart applications that involve handling JSON data from APIs.  The code attempts to decode a JSON response from an API; however, it lacks proper error handling for cases where the response is not valid JSON. This can lead to a `FormatException` crashing the app.

The `bug.dart` file contains the flawed code. The `bugSolution.dart` file provides a corrected version.

## Problem

The `jsonDecode` function in Dart throws a `FormatException` if the input string is not valid JSON. The original code doesn't handle this exception gracefully, resulting in app crashes.

## Solution

The solution involves adding more robust error handling.  We can check the response status code before attempting to decode the JSON.  More importantly we handle the `FormatException` specifically.  A user-friendly error message should be displayed instead of a program crash.