# Firestick Overscan Calibrator+

This Android application is an enhancement to Google's own overscan application which only allowed adjusting the overscan bars equally on all sides.

This enhanced application does the same behaviour, but also provides adjusting the top-right and bottom-left corners separately.

Since adjusting the overscan area requires special Android permissions to save/persist the changes, you either need root access or allow this application to write secure settings. Otherwise any changes that you make in the app won't be saved.

When te application launches and identifies that the needed permissions haven't been granted, then a popup will appear explaining what needs to be done.
Below is the ADB command needed to grant this application permissions to write the overscan changes into Android.
```
adb shell pm grant com.google.android.tungsten.overscan.plus android.permission.WRITE_SECURE_SETTINGS
```

The original Google Overscan application came from the Open GApps Project:
https://gitlab.opengapps.org/das_j/all/-/tree/e709de20d0d982873f722e925fda8595697fb14e/priv-app/com.google.android.tungsten.overscan

I downloaded and decompiled this application. I was then able to reassembe the code and I then enahnced it and changed the package name so it wouldn't collide with any preexisting applications/packages.

I would have uploaded my final source code, but my hard drive crashed and I lost everything, except this APK which I had installed on my phone.

This APK should run on Amazon Firestick TV 2nd generation devies without issue and the Xiaomi Mi Box 3 to.
It won't work on the NVIDIA Shield TV as it has its own version of this applicaiton built in, and it stores that overscan values in a different way.
