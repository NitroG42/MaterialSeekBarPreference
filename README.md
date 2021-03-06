## MaterialSeekBarPreference

[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-MaterialSeekBarPreference-brightgreen.svg?style=flat)](http://android-arsenal.com/details/1/1756)

As far as I checked, there are no cool implementations of SeekBarPreference. So I decided to make one.

![on LOLIPOP](https://raw.githubusercontent.com/MrBIMC/MaterialSeekBarPreference/master/SCREENSHOT_LP_511.png)
![on LOLIPOP with keyboard input](https://raw.githubusercontent.com/MrBIMC/MaterialSeekBarPreference/master/SCREENSHOT_LP_511_keyboard.png)
![on ICS](https://raw.githubusercontent.com/MrBIMC/MaterialSeekBarPreference/master/SCREENSHOT_ICS_404.png)

#Usage

Add this to your module dependencies:
```groovy
    compile 'com.pavelsikun:material-seekbar-preference:0.9+'
````

Reference namespace on top of your preferences layout file:
```xml
    xmlns:sample="http://schemas.android.com/apk/res-auto">
````

Now you can use this view in your preferences layout, just like any other normal preference.
```xml
    <com.pavelsikun.seekbarpreference.SeekBarPreference
        android:key="your_pref_key"
        android:title="SeekbarPreference 2"
        android:summary="Some summary"
        android:enabled="false"
        android:defaultValue="5000"
        sample:minValue="100"
        sample:maxValue="10000"
        sample:interval="200"
        sample:measurementUnit="%"/>
````

As you can see, lib provides 4 custom attributes(minValue, maxValue, interval and measurementUnit).
measurementUnit is should be String or a reference to a String (measurementUnit="%"  or measurementUnit="@string/my_preference_unit").
Every other attribute should be an Integer or reference to an Integer resource (interval="@integer/my_preference_interval" or interval="10").
Use them to define look and desired behavior of your preference.

#Known bugs and planned features
1. ~~Seekbar is not themmable on pre-lollipop.~~ DONE(v0.6+).
2. No support of RTL yet.
3. Small bug: It takes 2 taps on seekbar value indicator to open up the keyboard.

# Collaborators
I'd really want to thank:

* [krage](https://github.com/krage) for adding support for referenced resources.

#Licence
Lib is licenced under *MIT licence*, so you can do whatever you want with it.
I'd highly recommend to push changes back to make it cooler :D

