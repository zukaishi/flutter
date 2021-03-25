# flutter

https://flutter.dev/docs/get-started/install/macos
-  export PATH="$PATH:`pwd`/flutter/bin"
-  flutter doctor

```
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from:
      https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK
      components.
      (or visit https://flutter.dev/docs/get-started/install/macos#android-setup
      for detailed instructions).
      If the Android SDK has been installed to a custom location, please use
      `flutter config --android-sdk` to update to that location.

[!] Xcode - develop for iOS and macOS
    ✗ CocoaPods not installed.
        CocoaPods is used to retrieve the iOS and macOS platform side's plugin
        code that responds to your plugin usage on the Dart side.
        Without CocoaPods, plugins will not work on iOS or macOS.
        For more info, see https://flutter.dev/platform-plugins
      To install see
      https://guides.cocoapods.org/using/getting-started.html#installation for
      instructions.
[✓] Chrome - develop for the web
[!] Android Studio (not installed)
[✓] VS Code (version 1.54.2)
[✓] Connected device (1 available)
```
- brew update
- brew install cocoapods
- pod setup

- https://developer.android.com/studio からインストール
- (1)Android Studioを開く
- (2)ヘッダー部分の『Android Studio』をクリック
- (3)preferenceをクリック
- (4)Pluginsをクリック
- (5)検索画面でflutterを検索、ダウンロード

-  flutter doctor
```
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 2.0.3, on macOS 11.2.2 20D80 darwin-x64, locale ja-JP)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/docs/get-started/install/macos#android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, please use
      `flutter config --android-sdk` to update to that location.

[✓] Xcode - develop for iOS and macOS
[✓] Chrome - develop for the web
[✓] Android Studio (version 4.1)
[✓] VS Code (version 1.54.2)
[✓] Connected device (1 available)
```

- Android Studioセットアップを実行インストール
```
[!] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
    ✗ Android license status unknown.
      Run `flutter doctor --android-licenses` to accept the SDK licenses.
      See https://flutter.dev/docs/get-started/install/macos#android-setup for more details.
[✓] Xcode - develop for iOS and macOS
[✓] Chrome - develop for the web
[✓] Android Studio (version 4.1)
[✓] VS Code (version 1.54.2)
[✓] Connected device (1 available)

! Doctor found issues in 1 category.
```

- flutter doctor --android-licenses
```
ERROR: JAVA_HOME is set to an invalid directory: /usr/libexec/java_home -v 1.8

Please set the JAVA_HOME variable in your environment to match the
location of your Java installation.
```
- export JAVA_HOME=`/usr/libexec/java_home -v 14.0.2`
```
Exception in thread "main" java.lang.NoClassDefFoundError: javax/xml/bind/annotation/XmlSchema
	at com.android.repository.api.SchemaModule$SchemaModuleVersion.<init>(SchemaModule.java:156)
	at com.android.repository.api.SchemaModule.<init>(SchemaModule.java:75)
	at com.android.sdklib.repository.AndroidSdkHandler.<clinit>(AndroidSdkHandler.java:81)
	at com.android.sdklib.tool.sdkmanager.SdkManagerCli.main(SdkManagerCli.java:73)
	at com.android.sdklib.tool.sdkmanager.SdkManagerCli.main(SdkManagerCli.java:48)
Caused by: java.lang.ClassNotFoundException: javax.xml.bind.annotation.XmlSchema
	at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:602)
	at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:178)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:522)
	... 5 more
```
