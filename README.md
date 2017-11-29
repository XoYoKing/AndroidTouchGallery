支持双击或双指缩放的Gallery(用ViewPager实现)，相比下面的PhotoView，在被放大后依然能滑到下一个item，并且支持直接从url和文件中获取图片，
项目地址：https://github.com/Dreddik/AndroidTouchGallery
Demo地址：https://github.com/Trinea/TrineaDownload/blob/master/touch-gallery-demo.apk?raw=true
APP示例：类似微信中查看聊天记录图片时可双击放大，并且放大情况下能正常左右滑动到前后图片

Attention please!
===================
This library is not supported anymore. Please, check out nice living forks!
Thanks for attention.


AndroidTouchGallery
===================

Android widget for gallery, using viewpager. Allow pinch zoom and drag for images by url.
Widget allows use it in Android > 2.0!


How to use
===================
1. Make import library folder into your IDE.
2. Make sure, that AndroidTouchGallery has included in your project as library. Check project properties, and make sure checkbox "Is library" is checked.
3. Include GalleryViewPager in your layout xml or programmatically.
```
<ru.truba.touchgallery.GalleryWidget.GalleryViewPager
     android:id="@+id/viewer"
     android:layout_width="fill_parent"
     android:layout_height="fill_parent"
     />
```

4. Provide one of library adapters: UrlPagerAdapter or FilePagerAdapter
For example (an Activity code): 
```java
setContentView(R.layout.main);
String[] urls = {
    "http://cs407831.userapi.com/v407831207/18f6/jBaVZFDhXRA.jpg",
    "http://cs407831.userapi.com/v4078f31207/18fe/4Tz8av5Hlvo.jpg", //special url with error
    "http://cs407831.userapi.com/v407831207/1906/oxoP6URjFtA.jpg",
    "http://cs407831.userapi.com/v407831207/190e/2Sz9A774hUc.jpg",
    "http://cs407831.userapi.com/v407831207/1916/Ua52RjnKqjk.jpg",
    "http://cs407831.userapi.com/v407831207/191e/QEQE83Ok0lQ.jpg"
};
List<String> items = new ArrayList<String>();
Collections.addAll(items, urls);
UrlPagerAdapter pagerAdapter = new UrlPagerAdapter(this, items);  
GalleryViewPager mViewPager = (GalleryViewPager)findViewById(R.id.viewer);
mViewPager.setOffscreenPageLimit(3);
mViewPager.setAdapter(pagerAdapter);
```

5. You can always check example if you miss something.

License
===================
Copyright (c) 2012-2013 Roman Truba

 Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
 documentation files (the "Software"), to deal in the Software without restriction, including without limitation
 the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to
 permit persons to whom the Software is furnished to do so, subject to the following conditions:

 The above copyright notice and this permission notice shall be included in all copies or substantial
 portions of the Software.

 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED
 TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL
 THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
 WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
 THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
