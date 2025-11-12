package com.example.vetapp;

import android.os.Bundle;
import android.widget.ArrayAdapter;
import android.widget.Button;
import android.widget.EditText;
import android.widget.ListView;
import android.widget.SeekBar;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText wpis_wlasciciel, wpis_cel, wpis_czas;
    TextView tekst_wiek, tekst_wynik;
    SeekBar suwak_wiek;
    ListView lista_gatunek;
    String wybranyGatunek = "";

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        wpis_wlasciciel = findViewById(R.id.wpis_wlasciciel);
        wpis_cel = findViewById(R.id.wpis_cel);
        wpis_czas = findViewById(R.id.wpis_czas);
        tekst_wiek = findViewById(R.id.tekst_wiek);
        tekst_wynik = findViewById(R.id.tekst_wynik);
        suwak_wiek = findViewById(R.id.suwak_wiek);
        lista_gatunek = findViewById(R.id.lista_gatunek);
        Button przycisk_ok = findViewById(R.id.przycisk_ok);

        String[] gatunki = {"Pies", "Kot", "Świnka morska"};
        ArrayAdapter<String> adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, gatunki);
        lista_gatunek.setAdapter(adapter);

        lista_gatunek.setOnItemClickListener((parent, view, position, id) -> {
            wybranyGatunek = gatunki[position];
            if (wybranyGatunek.equals("Pies")) suwak_wiek.setMax(18);
            else if (wybranyGatunek.equals("Kot")) suwak_wiek.setMax(20);
            else suwak_wiek.setMax(9);
            suwak_wiek.setProgress(0);
            tekst_wiek.setText("0");
        });

        suwak_wiek.setOnSeekBarChangeListener(new SeekBar.OnSeekBarChangeListener() {
            @Override public void onProgressChanged(SeekBar seekBar, int progress, boolean b) {
                tekst_wiek.setText(String.valueOf(progress));
            }
            @Override public void onStartTrackingTouch(SeekBar seekBar) {}
            @Override public void onStopTrackingTouch(SeekBar seekBar) {}
        });

        przycisk_ok.setOnClickListener(v -> {
            String wynik = wpis_wlasciciel.getText() + ", " + wybranyGatunek + ", " +
                    tekst_wiek.getText() + ", " + wpis_cel.getText() + ", " + wpis_czas.getText();
            tekst_wynik.setText(wynik);
        });
    }
}
