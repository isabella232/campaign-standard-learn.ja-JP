---
title: 手順2 — モバイルSDKの統合
description: この部分では、AndroidアプリをモバイルSDKと統合します。 モバイルSDKとAndroidアプリを統合するには
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: c3ff1a137fb8ee9506a11f82e1a27d010bbd97e6
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# 手順2 - Androidアプリ [!UICONTROL Mobile SDK] との統合

この部分では、 [!DNL Android] アプリをと統合し [!UICONTROL Mobile SDK]ます。 アプリ [!UICONTROL mobile SDK] と統合するに [!DNL Android] は、次の手順に従います。

* 次の場所で *ACSPushTutorial* プロジェクトを開きます。 [!DNL Android Studio]
* 拡張するMainAppという新しいJavaクラス *を作成します* 。 [!DNL android.app.Application]
* この時点でのプロジェクト構造は次のようになります

![メインアプリ](assets/android-main-app.PNG)

* フォルダを展開し [!DNL Gradle Scripts] ます。 重複がモジュール [!DNL build.gradle] のをクリックします。 次の依存関係を、フ [!DNL build.gradle] ァイルの依存関係セクションに貼り付けます。 これで、 [!DNL build.gradle] ファイルは次のようになります

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![モジュール・グレーダル](assets/module-build-gradle.PNG)

* 「今すぐ同期」ボタンをクリックしてプロジェクトを同期し、 [!DNL Android] プロジェクトを同期します

## 修正 [!DNL AndroidManifest.xml]{#modify-android-manifest}

AndroidManifest.xml *を開き* 、manifest要素の後、およびapplication要素の前に、以下の2行を貼り付けます。 これにより、アプリケーションが外部の世界と通信できるようになります

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

アプリケーション要素に次の行をコピーし[!DNL android:name=".MainApp"]ます。 [!DNL AndroidManifest.xml]「保存」は、次のよう [!DNL AndroidManifest.xml] に表示されます。

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
