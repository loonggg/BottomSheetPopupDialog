# BottomSheetPopupDialog
这是一个底部弹出框的库。使用方法也非常简单。
### 效果图，如下：
![](https://raw.githubusercontent.com/loonggg/BottomSheetPopupDialog/master/image/ss.gif)
### Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:
```java
	allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
  ```

### Step 2. Add the dependency
```java
	dependencies {
	        compile 'com.github.loonggg:BottomSheetPopupDialog:v1.0'
	}
  ```
  BottomSheetPopupDialog和官方的 BottomSheetDialog非常相似，用法也非常相似。我们可以自定义dialog的布局，然后获取做相应的操作。
  ```java
  View dialogView = LayoutInflater.from(this).inflate(R.layout.share_bottom_dialog, null);
  ShareBottomPopupDialog shareBottomPopupDialog = new ShareBottomPopupDialog(this, dialogView);
  shareBottomPopupDialog.showPopup(all_layout);
  ```
  share_bottom_dialog.xml就是我们自定义的dialog的布局，然后在new ShareBottomPopupDialog时，放进去即可。然后调用showPopup(View rootview),方法显示。这里的view是所在页面的根布局。

