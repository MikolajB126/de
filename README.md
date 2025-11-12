<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp"
    android:background="#ADD8E6">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Właściwości czcionki"
        android:textSize="26sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginBottom="20dp"
        android:textColor="#000000" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Rozmiar:"
        android:textSize="18sp"
        android:layout_marginBottom="10dp"
        android:textColor="#000000" />

    <SeekBar
        android:id="@+id/seekRozmiar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginBottom="20dp"
        android:max="100"
        android:progress="20" />

    <TextView
        android:id="@+id/txtCytat"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="„To, co nas nie zabije, uczyni nas silniejszymi.”"
        android:textSize="20sp"
        android:gravity="center"
        android:textColor="#000080"
        android:layout_marginBottom="30dp" />

    <Button
        android:id="@+id/btnDalej"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text=">>"
        android:layout_gravity="center"
        android:background="#4169E1"
        android:textColor="#FFFFFF"
        android:textSize="18sp"
        android:paddingLeft="20dp"
        android:paddingRight="20dp" />

</LinearLayout>
