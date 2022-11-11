## Android develop problems solving

##### RecycleView中item间距异常大

自定义布局要match_content

##### BottomNavigation中Fragment自刷新后导致监听失效

activity?.findViewById改为view?.findViewById

##### MaterialButton最小化

android:minHeight="0dp"

##### MaterialButton背景色

backgroundTint

##### 子线程不让对UI更改，不让发起Toast

handler;   Looper.prepare()和Lopper.loop()

##### 软键盘把BottomNavigation顶上去了

对应的activity在清单中添加`android:windowSoftInputMode="adjustPan"`

