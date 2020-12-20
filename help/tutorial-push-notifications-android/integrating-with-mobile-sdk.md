---
title: 手順 2 - モバイル SDK を統合
description: この部分では、AndroidアプリをモバイルSDKと統合します。 モバイルSDKとAndroidアプリを統合するには
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# 手順2 - [!UICONTROL Mobile SDK]をAndroidアプリと統合する

この部分では、[!DNL Android]アプリを[!UICONTROL Mobile SDK]と統合します。 [!UICONTROL mobile SDK]を[!DNL Android]アプリと統合するには、次の手順に従ってください。

* [!DNL Android Studio]の&#x200B;*ACSPushTutorial*&#x200B;プロジェクトを開きます
* *MainApp*&#x200B;という名前の新しいJavaクラスを作成し、[!DNL android.app.Application]を拡張します。
* この時点でのプロジェクト構造は次のようになります

![メインアプリ](assets/android-main-app.PNG)

* [!DNL Gradle Scripts]フォルダーを展開します。 重複はモジュールの[!DNL build.gradle]をクリックします。 次の依存関係を[!DNL build.gradle]ファイルの依存関係セクションに貼り付けます。 [!DNL build.gradle]ファイルは次のようになります

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![モジュール・グレーダル](assets/module-build-gradle.PNG)

* 「今すぐ同期」ボタンをクリックして[!DNL Android]プロジェクトを同期し、プロジェクトを同期します

## 修正 [!DNL AndroidManifest.xml]{#modify-android-manifest}

*AndroidManifest.xml*&#x200B;を開き、manifest要素の後、アプリケーション要素の前に、次の2行を貼り付けます。 これにより、アプリケーションが外部の世界と通信できるようになります

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

アプリケーション要素内の次の行をコピーします。
[!DNL android:name=".MainApp"]
[!DNL AndroidManifest.xml]を保存
[!DNL AndroidManifest.xml]は次のようになります

<!--
Removed `{.line-numbers}` below
-->

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
