#Godot-SpeechToText
- Speech-to-text support on Godot engine for Android, using the google speech api (https://github.com/okamstudio/godot)

- Godot version 2.0 stable.

##How to use
- Drop the speechtotext folder inside godot/modules

- Move the speechtotext/GodotSpeech.java to godot/platform/android/java/src/org/godotengine/godot

- Import the speechtest example project in Godot for a test run [ Not a great UI. Just functionality demonstration ]


**Note:** The speechtotext/android.jar is taken from  *android-sdk-linux/platforms/android-19*. You may choose to use any other api version.

###Compile
1. #> scons platform=android
2. cd godot/platform/android/java
3. #> ./gradlew build
4. The resulting apk will be available at godot/platform/android/java/build/outputs/apk
 
###Configure
Add the following in the engine.cfg file:

> [android]

> modules="org/godotengine/godot/GodotSpeech"

**Use them in the script:**

> var singleton = Globals.get_singleton("GodotSpeech")

> singleton.doListen() # opens up the mic ui

> singleton.getWords() # gets the strings of words 

###Build the game apk
From the settings of the godot engine UI:

> Export->Target->Android


Custom Package (Debug/Release): 
> Point to the newly built apk

> Permission check: RecordAudio

####License
MIT

###Special Mention
Thanks [TeamKrishna](http://teamkrishna.in) for the request.

Similar plugings: [GodotVibrate](https://github.com/literaldumb/GodotVibrate) 

