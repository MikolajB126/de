package com.example.urzadzeniadowe;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText editNrPrania;
    Button btnZatwierdz, btnWlacz;
    TextView txtNumerPrania, txtOdkurzaczStatus;
    boolean odkurzaczWlaczony = false;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editNrPrania = findViewById(R.id.editNrPrania);
        btnZatwierdz = findViewById(R.id.btnZatwierdz);
        txtNumerPrania = findViewById(R.id.txtNumerPrania);
        btnWlacz = findViewById(R.id.btnWlacz);
        txtOdkurzaczStatus = findViewById(R.id.txtOdkurzaczStatus);

        btnZatwierdz.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String tekst = editNrPrania.getText().toString();
                if (!tekst.isEmpty()) {
                    int numer = Integer.parseInt(tekst);
                    if (numer >= 1 && numer <= 12) {
                        txtNumerPrania.setText("Numer prania: " + numer);
                    } else {
                        txtNumerPrania.setText("Numer prania: nie podano");
                    }
                } else {
                    txtNumerPrania.setText("Numer prania: nie podano");
                }
            }
        });

        btnWlacz.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (!odkurzaczWlaczony) {
                    btnWlacz.setText("Wyłącz");
                    txtOdkurzaczStatus.setText("Odkurzacz włączony");
                    odkurzaczWlaczony = true;
                } else {
                    btnWlacz.setText("Włącz");
                    txtOdkurzaczStatus.setText("Odkurzacz wyłączony");
                    odkurzaczWlaczony = false;
                }
            }
        });
    }
}
