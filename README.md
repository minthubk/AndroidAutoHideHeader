# AndroidAutoHideHeader
[ ![Download](https://api.bintray.com/packages/vcaen/maven/androidautohideheader/images/download.svg) ](https://bintray.com/vcaen/maven/androidautohideheader/_latestVersion)

A layout that hide the header when the body is scrolled down and reveal it when the header is scrolled up

## Demo

![Demo gif](https://raw.githubusercontent.com/vcaen/AndroidAutoHideHeader/master/example.gif)

## Usage

### Programmatically 
In you xml, add the '''AutoHideHeaderLayout''' : 

```xml
    <com.vcaen.androidautohideheader.AutoHideHeaderLayout
        android:id="@+id/autohideview"
       android:layout_width="match_parent"
       android:layout_height="match_parent"/>
``` 

Then in your java code : 
 ```java
    AutoHideHeaderLayout view  = (AutoHideHeaderLayout) findViewById(R.id.autohideview);
    ListView listView = new ListView(this);
    view.setHeader(R.layout.header); // You can also set the View object
    view.setBodyView(listView);
```

### XML Only

You can add the childs directly into the XML by adding them inside the ```AutoHideHeaderLayout``` :
```xml
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
                xmlns:tools="http://schemas.android.com/tools"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                tools:context=".MainActivity">

    <com.vcaen.androidautohideheader.AutoHideHeaderLayout
        android:id="@+id/autohideview"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="100dp">

            <ImageView
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:scaleType="centerCrop"
                android:src="@drawable/bg"/>

        </RelativeLayout>

        <ScrollView
            android:layout_width="match_parent"
            android:layout_height="match_parent">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:orientation="vertical">

            </LinearLayout>
        </ScrollView>
    </com.vcaen.androidautohideheader.AutoHideHeaderLayout>

</RelativeLayout>
```


## Import it ! 


In your gradle "app" :

```
dependencies {
    compile 'com.vcaen:androidautohideheader:1.1'
}
```
```
