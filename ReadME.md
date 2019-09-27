https://fcm.googleapis.com/fcm/send

Content-Type: application/json
Authorization: key=AAAAn20fA3Q:APA91bHtl_CtrbWDCErXTg2t5sQI-rQFQoZrLkZWuWV6MoGyCFFFOMm6s77C7PirEaDDZ3xazTXen_VsXWZeU6ZTu9bvJYSCfYsvBXCmD7v5AdQin4gBSvdqplvc2usZtUOvt1f7T_b1

payload 
{
  "registration_ids":["c2lnJjywOqM:APA91bHVZMnktCuvYDA2a6VLwReA3eO6aYIvC0S7QUJFA3UewUI2wxEknAGhJjp38nCN1UQ9nJEN8tXHKv4klnm1JYA4KTDCjWNkLVm_B-4mXseObzPawI8zs2aCiCFJGEmnfJQC91eB"],
  "notification" : {
 "body" : "DONt Know WHY!",
 "title" : "Hey buddy",
 "content_available" : true,
 "priority" : "high"
 }
}

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