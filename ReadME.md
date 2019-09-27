https://fcm.googleapis.com/fcm/send

ERROR & resolution
#1 
android.useAndroidX=true
android.enableJetifier=true
project/android/gradle.properties

#2
The 401 error pertains that your Authorization Key is invalid or incorrect.

When using Postman, add a key= prefix for the value of Authorization, like so:

key=AAA...
See below for a tutorial on Sending Downstream FCM Messages using Postman.

Also, for your notification message payload, text isn't one of the valid parameters, I think you were looking for message instead.

https://mobikul.com/send-push-notification-via-firebase-ios-postman/
