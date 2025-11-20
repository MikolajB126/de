<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp"
    android:background="@android:color/white">

    <TextView
        android:id="@+id/tekstTytul"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Właściwości czcionki"
        android:textSize="28sp"
        android:textStyle="bold"
        android:padding="10dp"
        android:gravity="center"
        android:background="#558B2F"
        android:textColor="@android:color/white" />

    <TextView
        android:id="@+id/tekstRozmiar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Rozmiar:"
        android:textSize="20sp"
        android:textColor="@android:color/black"
        android:layout_marginTop="20dp"/>

    <SeekBar
        android:id="@+id/suwak"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:max="40" />

    <TextView
        android:id="@+id/tekstCytat"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Dzień dobry"
        android:textSize="16sp"
        android:layout_marginTop="10dp"
        android:textColor="@android:color/black" />

    <Button
        android:id="@+id/przyciskDalej"
        android:layout_width="120dp"
        android:layout_height="wrap_content"
        android:text=">>"
        android:background="#558B2F"
        android:textColor="@android:color/white"
        android:textStyle="bold"
        android:layout_gravity="center"
        android:layout_marginTop="20dp"/>
</LinearLayout>
dddddddddddddddddddddddddddddddd
package com.example.czcionki;

import android.os.Bundle;
import android.widget.Button;
import android.widget.SeekBar;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private TextView tekstRozmiar;
    private SeekBar suwak;
    private TextView tekstCytat;
    private Button przyciskDalej;

    private String[] cytaty = {"Dzień dobry", "Good morning", "Buenos dias"};
    private int indeks = 0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        tekstRozmiar = findViewById(R.id.tekstRozmiar);
        suwak = findViewById(R.id.suwak);
        tekstCytat = findViewById(R.id.tekstCytat);
        przyciskDalej = findViewById(R.id.przyciskDalej);

        suwak.setOnSeekBarChangeListener(new SeekBar.OnSeekBarChangeListener() {
            @Override
            public void onProgressChanged(SeekBar seekBar, int wartosc, boolean fromUser) {
                tekstRozmiar.setText("Rozmiar: " + wartosc);
                tekstCytat.setTextSize(wartosc);
            }

            @Override
            public void onStartTrackingTouch(SeekBar seekBar) { }

            @Override
            public void onStopTrackingTouch(SeekBar seekBar) { }
        });

        przyciskDalej.setOnClickListener(v -> {
            indeks = (indeks + 1) % cytaty.length;
            tekstCytat.setText(cytaty[indeks]);
        });
    }
}

