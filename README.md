<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="#558B2F"
    android:padding="20dp">

    <TextView
        android:id="@+id/txtTytul"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Właściwości czcionki"
        android:textColor="#FFFFFF"
        android:textStyle="bold"
        android:textSize="28sp"
        android:gravity="center"
        android:layout_marginBottom="20dp" />

    <TextView
        android:id="@+id/txtRozmiar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Rozmiar:"
        android:textColor="#FFFFFF"
        android:textSize="20sp"
        android:layout_marginBottom="10dp" />

    <SeekBar
        android:id="@+id/seekRozmiar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:max="40"
        android:progress="20"
        android:layout_marginBottom="20dp" />

    <TextView
        android:id="@+id/txtCytat"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Dzień dobry"
        android:textColor="#000000"
        android:textSize="20sp"
        android:gravity="center"
        android:layout_marginBottom="30dp" />

    <Button
        android:id="@+id/btnZmien"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text=">>"
        android:textStyle="bold"
        android:textColor="#000000"
        android:background="#FFFFFF"
        android:layout_gravity="center"
        android:paddingLeft="25dp"
        android:paddingRight="25dp"
        android:textSize="20sp" />
</LinearLayout>
