[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-SHSegmentControl-brightgreen.svg?style=flat)](http://android-arsenal.com/details/1/1770) [![jitpack](https://img.shields.io/github/tag/7heaven/SHSegmentControl.svg?label=JitPack%20Maven)](https://img.shields.io/github/release/7heaven/SHSegmentControl.svg?label=JitPack%20Maven) [![Build Status](http://img.shields.io/travis/7heaven/SHSegmentControl.svg)](https://travis-ci.org/7heaven/SHSegmentControl)
[![License](https://img.shields.io/badge/apache-2.0-orange.svg)](LICENSE)
[ ![Download](https://api.bintray.com/packages/7heaven/maven/SHSegmentControl/images/download.svg) ](https://bintray.com/7heaven/maven/SHSegmentControl/_latestVersion)

#a simple SegmentControl Widget

![art2](arts/arts2.gif)

![art1](arts/arts1.gif)

## 使用：

### 在 module 根目录的 build.gradle 中添加：

其中最后版本在 release 中查看，如：1.13
```groovy
dependencies {
    compile 'com.7heaven.widgets:segmentcontrol:1.13'
}
```

### 三、使用

set segmentControl's property using attrs,using '|' to separate segments.

``` xml
<com.sevenheaven.segmentcontrol.SegmentControl
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/segment_control"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="20dp"
    android:textSize="18sp"
    app:colors="#0099CC"
    app:cornerRadius="5dp"
    app:direction="vertical"
    app:horizonGap="10dp"
    app:separatorWidth="2dp"
    app:boundWidth="4dp"
    app:textSelectedColors="#E74C3C"
    app:texts="啊啊|啦啦啦|哈哈哈|顶顶顶顶"
    app:verticalGap="10dp"/>
```

using OnSegmentControlClickListener to listen to segment change event.

```java
mSegmentHorzontal = (SegmentControl) findViewById(R.id.segment_control);
mSegmentHorzontal.setOnSegmentControlClickListener(new SegmentControl.OnSegmentControlClickListener() {
    @Override
    public void onSegmentControlClick(int index) {
        Log.i(TAG, "onSegmentControlClick: index = " + index);
    }
});
```
