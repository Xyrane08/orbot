
This document explains how to properly build an Android package of Orbot from
source.

DECEMBER 2017: We have removed the build process for tor and polipo from Orbot,
and instead now use the new tor-android gradle dependency: https://github.com/n8fr8/tor-android

Orbot includes, in the external directory, git repo submodules of:
	- JTorControl: The Tor Control Library for Java

Please install the following prerequisites (instructions for each follows):
	ant: http://ant.apache.org/
	Android Native Dev Kit or NDK (for C/C++ code):
        http://developer.android.com/sdk/ndk/index.html
	Android Software Dev Kit or SDK (for Java code):
        http://developer.android.com/sdk/index.html

Be sure that you have all of the git submodules up-to-date:

	git submodule update --init --recursive

You then need to run "ndk-build" from:
	
	cd orbotservice/src/main
	ndk-build
	mv libs/armeabi-v7a/pdnsd libs/armeabi-v7a/pdnsd.so
	mv libs/arm64-v8a/pdnsd libs/arm64-v8a/pdnsd.so
	mv libs/x86/pdnsd libs/x86/pdnsd.so
	mv libs/x86_64/pdnsd libs/x86_64/pdnsd.so

Now build the Android app

(gradle / android studio instructions here)

This will produce an unsigned Orbot package APK.

To produce a usable package, you'll need to sign the .apk. The basics on
signing can be found on the Android developer site:

	http://developer.android.com/guide/publishing/app-signing.html


