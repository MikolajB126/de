<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="@color/zielony_tlo"
    android:padding="10dp">

    <TextView
        android:id="@+id/tekst_tytul"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/tytul"
        android:textSize="24sp"
        android:textStyle="bold"
        android:textColor="@color/bialy"
        android:padding="10dp"
        android:background="@color/zielony_tytul" />

    <EditText
        android:id="@+id/wpis_wlasciciel"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/wpis_wlasciciel_hint"
        android:layout_marginTop="10dp" />

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/gatunek"
        android:layout_marginTop="10dp" />

    <ListView
        android:id="@+id/lista_gatunek"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:divider="@android:color/darker_gray"
        android:dividerHeight="1dp" />

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="10dp">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/ile_lat" />

        <TextView
            android:id="@+id/tekst_wiek"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="0"
            android:layout_marginStart="5dp"/>
    </LinearLayout>

    <SeekBar
        android:id="@+id/suwak_wiek"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:max="20" />

    <EditText
        android:id="@+id/wpis_cel"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/cel_wizyty_hint"
        android:layout_marginTop="10dp" />

    <EditText
        android:id="@+id/wpis_czas"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/czas_domyslny"
        android:layout_marginTop="10dp" />

    <Button
        android:id="@+id/przycisk_ok"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/ok"
        android:layout_marginTop="15dp" />

    <TextView
        android:id="@+id/tekst_wynik"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="15dp"
        android:textColor="@color/czarny" />
</LinearLayout>
