# How to use this JAR file in Unity project

Note: Regarding JAR file creation and usage, please refer to [the Guideline](http://static.appstore.picovr.com/docs/JarUnity/index.html)

## ModifyAndroidManifest
Add permission  
```
<uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED" />
<uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW" />
```

## ClassName
```
android:name = "com.example.bootcomplete.MainActivity"
```
## Register system broadcast 

```
<receiver android:name="com.example.bootcomplete.BootReceiver" >
            <intent-filter android:priority="1000">
                <action android:name="android.intent.action.BOOT_COMPLETED" />
            </intent-filter>
</receiver>
```

Note: it is required to run the application before next device boot-up

