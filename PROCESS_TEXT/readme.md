# android.intent.action.PROCESS_TEXT

AndroidManifest.xml


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
                <action android:name="android.intent.action.VIEW" />
                <action android:name="android.intent.action.PROCESS_TEXT" />
                <category android:name="android.intent.category.DEFAULT" />
            </intent-filter>
        </activity>
        
    </application>
</manifest>
```

Java Code:

qz.userdictionary.ViewModel.TeksAction;

```java

String words = getIntent().getStringExtra(Intent.EXTRA_PROCESS_TEXT);
Toast.makeText(this, words, Toast.LENGTH_SHORT).show();

```


With am:

```bash
am start -a android.intent.action.PROCESS_TEXT -n qz.userdictionary/.ViewModel.TeksAction --es "android.intent.extra.PROCESS_TEXT" "Hello World"
```
