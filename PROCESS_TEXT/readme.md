# android.intent.action.PROCESS_TEXT

[AndroidManifest.xml](https://github.com/QiubyZ/QZ-UserDict/blob/dac2a5c2a9df8f0d1f6fe917790ddba7df7afb72/app/src/main/AndroidManifest.xml#L35)

```XML
<manifest
    ...
    <application 
    ...>
        <activity
            android:exported="true"
            android:name=".ViewModel.TeksAction">
            <intent-filter>
                <data android:mimeType="text/plain" />
                <action android:name="android.intent.action.PROCESS_TEXT" />
            </intent-filter>
        </activity>
        
    </application>
</manifest>
```


[Java Code](https://github.com/QiubyZ/QZ-UserDict/blob/dac2a5c2a9df8f0d1f6fe917790ddba7df7afb72/app/src/main/java/qz/userdictionary/ViewModel/TeksAction.java#L11):

qz.userdictionary.ViewModel.TeksAction;

```java

String words = getIntent().getStringExtra(Intent.EXTRA_PROCESS_TEXT);
Toast.makeText(this, words, Toast.LENGTH_SHORT).show();

```


With am:

```bash
am start -a android.intent.action.PROCESS_TEXT -n qz.userdictionary/.ViewModel.TeksAction --es "android.intent.extra.PROCESS_TEXT" "Hello World" -t text/plain
```

You can download my application to test it [here](https://github.com/QiubyZ/QZ-UserDict/releases)