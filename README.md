package com.example.calculator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import org.w3c.dom.Text;

public class MainActivity extends AppCompatActivity {
    private Button ADD;
    private TextView input1;
    private TextView input2;
    private TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        input1 = findViewById(R.id.input1);
        input2 = findViewById(R.id.input2);
        ADD =  findViewById(R.id.ADD);
        result = findViewById(R.id.result);


        ADD.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String a =input1.getText().toString();
                int x=Integer.parseInt(a);
                String b =input2.getText().toString();
                int y=Integer.parseInt(b);
                result.setText(x+y+"");
            }
        });


    }
}
