# Time to Compile

So in a terminal navigate to our tweak directory and type:

```bash
make package install
```

If you have followed all the instructions you should get an output like this
```bash
❯ make package install
> Making all for tweak ExampleTweak…
==> Preprocessing Tweak.x…
==> Compiling Tweak.x (arm64)…
==> Linking tweak ExampleTweak (arm64)…
ld: warning: building for iOS, but linking in .tbd file (/Users/kodeythomas/theos/vendor/lib/CydiaSubstrate.framework/CydiaSubstrate.tbd) built for iOS Simulator
==> Generating debug symbols for ExampleTweak…
rm /Users/kodeythomas/GitHub/exampletweak/.theos/obj/debug/arm64/Tweak.x.m
==> Preprocessing Tweak.x…
==> Compiling Tweak.x (arm64e)…
==> Linking tweak ExampleTweak (arm64e)…
ld: warning: building for iOS, but linking in .tbd file (/Users/kodeythomas/theos/vendor/lib/CydiaSubstrate.framework/CydiaSubstrate.tbd) built for iOS Simulator
==> Generating debug symbols for ExampleTweak…
rm /Users/kodeythomas/GitHub/exampletweak/.theos/obj/debug/arm64e/Tweak.x.m
==> Merging tweak ExampleTweak…
==> Signing ExampleTweak…
> Making stage for tweak ExampleTweak…
dm.pl: building package `com.kodeycodesstuff.exampletweak:iphoneos-arm' in `./packages/com.kodeycodesstuff.exampletweak_0.0.1-1+debug_iphoneos-arm.deb'
==> Installing…
Selecting previously unselected package com.kodeycodesstuff.exampletweak.
(Reading database ... 11304 files and directories currently installed.)
Preparing to unpack /tmp/_theos_install.deb ...
Unpacking com.kodeycodesstuff.exampletweak (0.0.1-1+debug) ...
Setting up com.kodeycodesstuff.exampletweak (0.0.1-1+debug) ...
Processing triggers for com.saurik.substrate.safemode (1.1) ...
==> Unloading SpringBoard…
```

And its done our first tweak is completed, if you try pressing the volume buttons on your phone you will notice they now have lovely haptic feedback

If we want to export our tweak to a repo it is saved as a `debian` file known as a `.deb`

The `.deb` is saved under `.../TweakName/packages/`

Its named under the default naming convention of the `bundleID` then the build number for example the tweak we have just compiled for me is saved as:

```UTF-8
com.kodeycodesstuff.exampletweak_0.0.1-1+debug_iphoneos-arm.deb
```

Now you have made your first tweak. Congratulations

Source Code for this example tweak can be found [here](https://github.com/KodeyThomas/ExampleTweak)
> Be sure to change THEOS_DEVICE_IP under the makefile otherwise it wont compile