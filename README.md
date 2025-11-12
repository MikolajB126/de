<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#ADD8E6">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="10dp">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Urządzenia Domowe"
            android:gravity="center"
            android:textSize="26sp"
            android:layout_margin="5dp"
            android:textColor="#000000" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Autor: 12345"
            android:gravity="center"
            android:textSize="18sp"
            android:layout_margin="5dp"
            android:textColor="#000000" />

        <ImageView
            android:layout_width="match_parent"
            android:layout_height="150dp"
            android:src="@drawable/pralka"
            android:layout_marginLeft="20dp"
            android:layout_marginRight="20dp"
            android:layout_marginBottom="20dp"
            android:scaleType="fitCenter" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Pralka"
            android:textSize="22sp"
            android:textColor="#000000"
            android:gravity="center" />

        <EditText
            android:id="@+id/editNrPrania"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="Podaj nr prania 1..12"
            android:inputType="number"
            android:textColor="#000080"
            android:textColorHint="#000080"
            android:background="#87CEEB"
            android:layout_marginTop="8dp"
            android:layout_marginBottom="8dp" />

        <Button
            android:id="@+id/btnZatwierdz"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Zatwierdź"
            android:background="#4169E1"
            android:textColor="#FFFFFF"
            android:textSize="18sp"
            android:layout_margin="10dp" />

        <TextView
            android:id="@+id/txtNumerPrania"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Numer prania: nie podano"
            android:textSize="16sp"
            android:gravity="center" />

        <ImageView
            android:layout_width="match_parent"
            android:layout_height="150dp"
            android:src="@drawable/odkurzacz"
            android:layout_marginLeft="20dp"
            android:layout_marginRight="20dp"
            android:layout_marginBottom="20dp"
            android:layout_marginTop="0dp"
            android:scaleType="fitCenter" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Odkurzacz"
            android:textSize="22sp"
            android:textColor="#000000"
            android:gravity="center" />

        <Button
            android:id="@+id/btnWlacz"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Włącz"
            android:background="#4169E1"
            android:textColor="#FFFFFF"
            android:textSize="18sp"
            android:layout_margin="10dp" />

        <TextView
            android:id="@+id/txtOdkurzaczStatus"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Odkurzacz wyłączony"
            android:textSize="16sp"
            android:gravity="center" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Status: naładowany"
            android:textSize="16sp"
            android:gravity="center"
            android:layout_marginTop="4dp" />
    </LinearLayout>
</ScrollView>
