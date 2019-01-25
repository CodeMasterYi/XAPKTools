# XAPKTools

Apk & exe file downloaded from: [APKPure](https://apkpure.com/apk-install.html "APKPure")

xapk struct:
```
- Android
    - obb
    - ${ApplicationId}
      main.${versionCode}.${ApplicationId}.obb
icon.png
manifest.json
${ApplicationId}.apk
```

manifest.json content:
```json
{
   "xapk_version":1,
   "package_name":"${ApplicationId}",
   "name":"${AppName}",
   "version_code":"${versionCode}",
   "version_name":"${versionName}",
   "min_sdk_version":"${minSdkVersion}",
   "target_sdk_version":"${targetSdkVersion}",
   "permissions":[
      "android.permission.INTERNET"
   ],
   "total_size":${apkSize + obbSize},
   "expansions":[
      {
         "file":"Android/obb/${ApplicationId}/main.${versionCode}.${ApplicationId}.obb",
         "install_location":"EXTERNAL_STORAGE",
         "install_path":"Android/obb/${ApplicationId}/main.${versionCode}.${ApplicationId}.obb"
      }
   ]
}
```
