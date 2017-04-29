WebRTC Framework
=================


* [Android](#Android)
* [IOS](#IOS)
* [OSX](#OSX/Mac)


## Android:

Fraework is generated with following command on M58 branch (Apr'2017)
for armeabi-v7a, arm64-v8a, x86 & x86_64 architectures
	
	./tools-webrtc/android/build_aar.py --arch 'armeabi-v7a' 'arm64-v8a' 'x86' 'x86_64'
	
	AndroidStudio Setup:
	Include the libwebrtc.aar into your AndroidStudio in the following way

	File -> New -> New Module -> Import .JAR/.AAR Package -> Next -> Choose the downloaded file
	Then compile libwebrtc in dependencies section of your aap build.gradle file.
	
	Example:
		dependencies {
		    compile fileTree(include: ['*.jar'], dir: 'libs')
		    androidTestCompile('com.android.support.test.espresso:espresso-core:2.2.2', {
			exclude group: 'com.android.support', module: 'support-annotations'
		    })
		    compile 'com.android.support:appcompat-v7:25.3.1'
		    compile 'com.android.support.constraint:constraint-layout:1.0.2'
		    testCompile 'junit:junit:4.12'
		    compile project(':libwebrtc')
		    compile files('libs/autobanh.jar')
		}

	Note: You can build the same by following instaructions at https://webrtc.org/native-code/android/
	
## IOS:

WebRTC.framework is generated with following commands on M58 branch (Apr'2017)
For armv7 & arm64 architectures
	
	./tools-webrtc/ios/build_ios_libs.sh	
	
	Xcode Setup:
	Include WebRTC.framework in Xcode Embedded Binaries
	Add WebRTC.framework/Headers in Header Search Paths of Build Settings
	
	Note: You can build the same by following instaructions at https://webrtc.org/native-code/ios/

## OSX/Mac: 
	WebRTC.framework is generated in Oct'2016 for X86_64 architecture
	For Xcode setup follow the instructions of IOS 
