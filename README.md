# android-java
jogo da velha 

Projeto concluido- Imagem 

![image](https://user-images.githubusercontent.com/72118415/120164546-16379880-c1d1-11eb-9782-d6751bf4179b.png)


1-	activity_main.xml.

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@android:color/holo_purple"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/btn11"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_above="@id/btn22"
        android:layout_toLeftOf="@id/btn22"
        android:textColor="@color/white" />

    <Button
        android:id="@+id/btn12"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_above="@id/btn22"
        android:layout_centerHorizontal="true" />

    <Button
        android:id="@+id/btn13"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_above="@id/btn22"
        android:layout_toRightOf="@id/btn22" />

    <Button
        android:id="@+id/btn22"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true" />

    <Button
        android:id="@+id/btn23"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        android:layout_toRightOf="@id/btn22" />

    <Button
        android:id="@+id/btn21"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        android:layout_toLeftOf="@id/btn22" />

    <Button
        android:id="@+id/btn31"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/btn22"
        android:layout_toLeftOf="@id/btn22" />

    <Button
        android:id="@+id/btn32"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/btn22"
        android:layout_centerHorizontal="true" />

    <Button
        android:id="@+id/btn33"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/btn22"
        android:layout_toRightOf="@id/btn22" />

    <Button
        android:id="@+id/btnReset"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_centerHorizontal="true"
        android:text="Reset" />

    <TextView
        android:id="@+id/txtJogador"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"
        android:text="Jogador: X"
        android:textAlignment="center"
        android:textColor="@color/white"
        android:textSize="30dp" />
</RelativeLayout>




MainActivity.java


package com.example.jogodavelha;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
    String jogador = "X";
    public void trocaJogador()
    {
        if(jogador.equals("X"))
        {
            jogador = "O";
        }
        else
        {
            jogador = "X";
        }
    }
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        getSupportActionBar().hide();
        final Button btn11Prog = (Button) findViewById(R.id.btn11);
        final Button btn12Prog = (Button) findViewById(R.id.btn12);
        final Button btn13Prog = (Button) findViewById(R.id.btn13);
        final Button btn22Prog = (Button) findViewById(R.id.btn22);
        final Button btn23Prog = (Button) findViewById(R.id.btn23);
        final Button btn21Prog = (Button) findViewById(R.id.btn21);
        final Button btn31Prog = (Button) findViewById(R.id.btn31);
        final Button btn32Prog = (Button) findViewById(R.id.btn32);
        final Button btn33Prog = (Button) findViewById(R.id.btn33);
        final TextView txtJogadorProg = (TextView) findViewById(R.id.txtJogador);
        final Button btnResetProg = (Button) findViewById(R.id.btnReset);
        btn11Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn11Prog.setText(jogador);
                trocaJogador();
                btn11Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });
        btn12Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn12Prog.setText(jogador);
                trocaJogador();
                btn12Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });

        btn13Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn13Prog.setText(jogador);
                trocaJogador();
                btn13Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });

        btn22Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn22Prog.setText(jogador);
                trocaJogador();
                btn22Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });
        btn23Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn23Prog.setText(jogador);
                trocaJogador();
                btn23Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });btn21Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn21Prog.setText(jogador);
                trocaJogador();
                btn21Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });
        btn31Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn31Prog.setText(jogador);
                trocaJogador();
                btn31Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });
        btn32Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn32Prog.setText(jogador);
                trocaJogador();
                btn32Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });
        btn33Prog.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn33Prog.setText(jogador);
                trocaJogador();
                btn33Prog.setClickable(false);
                txtJogadorProg.setText("Jogador: "+jogador);
            }
        });


        btnResetProg.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                btn11Prog.setClickable(true);
                btn11Prog.setText("");
                btn12Prog.setClickable(true);
                btn12Prog.setText("");
            }
        });
    }
}



![image](https://user-images.githubusercontent.com/72118415/120165059-8e9e5980-c1d1-11eb-94e4-9c0e6be85ea2.png)



