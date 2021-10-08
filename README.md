# EasingInterpolator
[![Platform](https://img.shields.io/badge/platform-android-green.svg)](http://developer.android.com/index.html)
<img src="https://img.shields.io/badge/license-MIT-green.svg?style=flat">
[![API](https://img.shields.io/badge/API-14%2B-yellow.svg?style=flat)](https://android-arsenal.com/api?level=14)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-EasingInterpolator-green.svg?style=true)](http://android-arsenal.com/details/1/3300)

Thirty-one different easing animation interpolators for Android.<br>
It does not use the standard 4 param ease signature. Instead it uses a single param which indicates the current linear ratio (0 to 1) of the tween. 

# Gradle
Add it in your root build.gradle at the end of repositories:
```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
Add the dependency to your build.gradle.
```groovy
dependencies {
    //implementation 'com.daasuu:EasingInterpolator:1.3.0'
    implementation 'com.github.kojofosu:EasingInterpolator:1.3.1'
}
```
# Usage
```JAVA

    ValueAnimator valueAnimator = new ValueAnimator();
    valueAnimator.setInterpolator(new EasingInterpolator(Ease.CUBIC_IN));
    valueAnimator.start();

    ObjectAnimator animator = ObjectAnimator.ofFloat(view, "translationY", 0, 300);
    animator.setInterpolator(new EasingInterpolator(Ease.ELASTIC_IN_OUT)));
    animator.start();

```
# Easing Graphs
<img src="art/easing.png" width="100%">
<img src="art/expo.png" width="60%">
<img src="art/FPSAnimator1.gif" width="70%">

# ProGuard
```
-keep class com.daasuu.** { *; }
```

## License

Copyright 2015 MasayukiSuda

`MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

`
