package com.example.listaelementow;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.ArrayAdapter;
import android.widget.Button;
import android.widget.ListView;
import java.util.ArrayList;
import java.util.Arrays;

public class MainActivity extends AppCompatActivity {

    ListView listView;
    Button btnDodaj;
    ArrayList<String> listaElementow;
    ArrayAdapter<String> adapter;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        listView = findViewById(R.id.listView);
        btnDodaj = findViewById(R.id.btnDodaj);

        String[] elementy = {"Element1", "Element2", "Element3"};
        listaElementow = new ArrayList<>(Arrays.asList(elementy));

        adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, listaElementow);
        listView.setAdapter(adapter);

        btnDodaj.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                listaElementow.add("nowy");
                adapter.notifyDataSetChanged();
            }
        });
    }
}
