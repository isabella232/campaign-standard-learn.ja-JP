---
title: 手順 2 - Mobile SDK の統合
description: ここでは、Android アプリを Mobile SDK と統合します。 モバイル SDK を Android アプリと統合するには：
feature: Push
user: Admin
level: Experienced
jira: KT-4826
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: 913d2c08dc63e2073b3abd1de6b6b16711d817da
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# 手順 2 — 統合 [!UICONTROL Mobile SDK] Android アプリを使用

この部分では、 [!DNL Android] 次のアプリ [!UICONTROL Mobile SDK]. 統合するには [!UICONTROL mobile SDK] と [!DNL Android] アプリの場合は、次の手順に従ってください。

* を開きます。 *ACSPushTutorial* ～に投じる [!DNL Android Studio]
* という新しい Java クラスを作成します。 *MainApp* 拡張する [!DNL android.app.Application]
* この時点でのプロジェクト構造は次のようになります

![メインアプリ](assets/android-main-app.PNG)

* を展開します。 [!DNL Gradle Scripts] フォルダー。 次をダブルクリックします。 [!DNL build.gradle] モジュールの。 次の依存関係を、の依存関係セクションに貼り付けます。 [!DNL build.gradle] ファイル。 お使いの [!DNL build.gradle] ファイルは次のようになります。

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![module-gradle](assets/module-build-gradle.PNG)

* を同期 [!DNL Android] 「今すぐ同期」ボタンをクリックしてプロジェクトを同期する

## 変更 [!DNL AndroidManifest.xml]{#modify-android-manifest}

開く *AndroidManifest.xml* 次の 2 行を manifest 要素の後、application 要素の前に貼り付けます。 これにより、アプリが外部と通信できるようになります

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

アプリケーション要素内の次の行をコピーします。
[!DNL android:name=".MainApp"]
を保存します。 [!DNL AndroidManifest.xml]
お使いの [!DNL AndroidManifest.xml] 次のようになります

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
