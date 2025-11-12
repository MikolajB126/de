<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="#ADD8E6"
    android:padding="16dp">

    <ListView
        android:id="@+id/listView"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:textSize="30sp"
        android:dividerHeight="2dp"
        android:divider="@android:color/transparent"/>

    <Button
        android:id="@+id/btnDodaj"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Dodaj"
        android:textSize="20sp"
        android:layout_marginTop="8dp"/>
</LinearLayout>
