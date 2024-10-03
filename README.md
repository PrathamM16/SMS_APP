# SMS Sender App

This is a simple Android application to send SMS messages. The app prompts the user for a phone number and message, then sends an SMS using the device's default SMS service.

## Features
- Enter a phone number and a message in the app.
- Send an SMS message to the entered phone number.
- Request necessary permissions to send SMS from the app.
- Displays toast messages for success or failure (including permission denial).

## Files and Components

### 1. MainActivity.kt

This file handles the app's main functionality, including:
- Managing user input (phone number and message).
- Requesting SMS permissions.
- Sending SMS via the `SmsManager` API.

### 2. activity_main.xml

This layout file provides a simple user interface with:
- An EditText for the phone number.
- An EditText for the message.
- A Button to trigger the SMS sending functionality.

### 3. AndroidManifest.xml

This file requires you to declare permissions to send SMS messages. Make sure to add the following permissions to the `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.SEND_SMS" />
<uses-feature android:name="android.hardware.telephony" android:required="false" />
