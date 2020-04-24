![Android CI](https://github.com/belljay/SwitchButton/workflows/Android%20CI/badge.svg)
[![](https://jitpack.io/v/belljay/SwitchButton.svg)](https://jitpack.io/#belljay/SwitchButton)
[![](https://img.shields.io/badge/minSdkVersion-11-brightgreen)](https://shields.io/)
[![](https://img.shields.io/badge/targetSdkVersion-29-blue)](https://shields.io/)

# SwitchButton

Note: this repo is forked and fixed forward on top of the awesome repo of [zcweng/SwitchButton](https://github.com/zcweng/SwitchButton).

- Ugraded API level to 29 so that it's compatiable with latest Google Play store requirements.
- Codebase is also upgraded to AndroidX for latest reference.
- Upgraded to support release from jitpack.io for easier installation on android apps.
- Add Proguards
- Add support for set button color programatically
- Some minor discrepency is also fixed.

SwitchButton.An *beautiful+lightweight+custom-style-easy* switch widget for Android,minSdkVersion >= 11<br>
issues welcome~<br>
![](21879.gif)<br>

Features
-------
-depend without third-part library<br>
-without raw files(pictures/drawables etc...), only one java and style.xml file<br>
-drag switch supported<br>


Integration
-------
gradle:
```grovvy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
...

dependencies {
    implementation 'com.github.belljay:SwitchButton:1.0.1'
}
```

maven:
```
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
...

<dependency>
    <groupId>com.github.belljay</groupId>
    <artifactId>SwitchButton</artifactId>
    <version>1.0.1</version>
</dependency>
```

Useage
-------
layout.xml:
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              android:layout_width="match_parent"
              android:layout_height="match_parent"
              xmlns:app="http://schemas.android.com/apk/res-auto"
              android:orientation="vertical">

    <com.suke.widget.SwitchButton
        android:id="@+id/switch_button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

</LinearLayout>
```

Activity.java:
```java
com.suke.widget.SwitchButton switchButton = (com.suke.widget.SwitchButton)
    findViewById(R.id.switch_button);

switchButton.setChecked(true);
switchButton.isChecked();
switchButton.toggle();     //switch state
switchButton.toggle(false);//switch without animation
switchButton.setShadowEffect(true);//disable shadow effect
switchButton.setEnabled(false);//disable button
switchButton.setEnableEffect(false);//disable the switch animation
switchButton.setOnCheckedChangeListener(new SwitchButton.OnCheckedChangeListener() {
    @Override
    public void onCheckedChanged(SwitchButton view, boolean isChecked) {
        //TODO do your job
    }
});


```

More Style:
```xml
<attr name="sb_shadow_radius" format="reference|dimension"/>       阴影半径  /  Shadow Radius
<attr name="sb_shadow_offset" format="reference|dimension"/>       阴影偏移  /  Shadow Position Offset
<attr name="sb_shadow_color" format="reference|color"/>            阴影颜色  /  Shadow Color
<attr name="sb_uncheck_color" format="reference|color"/>           关闭颜色  /  Unchecked Color
<attr name="sb_checked_color" format="reference|color"/>           开启颜色  /  Checked Color
<attr name="sb_border_width" format="reference|dimension"/>        边框宽度  /  Border Thickness
<attr name="sb_checkline_color" format="reference|color"/>         开启指示器颜色  /  Checked Indicator Line Color
<attr name="sb_checkline_width" format="reference|dimension"/>     开启指示器线宽  /  Checked Indicator Line Thickness
<attr name="sb_uncheckcircle_color" format="reference|color"/>     关闭指示器颜色  /  unchecked Indicator Cicle Color
<attr name="sb_uncheckcircle_width" format="reference|dimension"/> 关闭指示器线宽  /  unchecked Indicator Cicle Thickness
<attr name="sb_uncheckcircle_radius" format="reference|dimension"/>关闭指示器半径  /  unchecked Indicator Cicle Radius
<attr name="sb_checked" format="reference|boolean"/>               是否选中   /  is checked
<attr name="sb_shadow_effect" format="reference|boolean"/>         是否启用阴影  /  Turn on Shadow
<attr name="sb_effect_duration" format="reference|integer"/>       动画时间，默认300ms  /  Animation Duration, default 300ms
<attr name="sb_button_color" format="reference|color"/>            按钮颜色  /  Button Color
<attr name="sb_checkedbutton_color" format="reference|color"/>     开启按钮颜色  /  Checked Button Color
<attr name="sb_uncheckbutton_color" format="reference|color"/>     关闭按钮颜色  /  Unchecked Button Color
<attr name="sb_show_indicator" format="reference|boolean"/>        是否显示指示器，默认true  /  enable indicator, default: true
<attr name="sb_background" format="reference|color"/>              背景色，默认白色  / Background color, default white
<attr name="sb_enable_effect" format="reference|boolean"/>         是否启用特效，默认true / Enable Effect, default true
```


ScreenShot
-------
<a href="https://github.com/zcweng/SwitchButton/blob/master/sample/sample-debug.apk">Sample Apk:</a><br>
![](http://qr.api.cli.im/qr?data=https%253A%252F%252Fgithub.com%252Fzcweng%252FSwitchButton%252Fblob%252Fmaster%252Fsample%252Fsample-debug.apk&level=H&transparent=false&bgcolor=%23ffffff&forecolor=%23000000&blockpixel=12&marginblock=1&logourl=&size=280&kid=cliim&key=8144f9f150d38d7d364c923d0b9c87cf)<br>
![](device-capture.png)


License
-------
MIT, See the <a href="https://github.com/zcweng/SwitchButton/blob/master/LICENSE">[LICENSE]</a> file for details.
