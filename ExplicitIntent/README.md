# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by:Santhosh Kumar B
Registeration Number :212221040146
*/
```
**MainActivity.java:**

package com.example.experiment_4;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;

import android.os.Bundle;

import android.view.View;

import android.widget.EditText;

public class MainActivity extends AppCompatActivity
{

    EditText etNumber;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        etNumber=findViewById(R.id.etNumber);
    }
    public void displayFactorial(View view){
        Intent i = new Intent(MainActivity.this,MainActivity2.class);
        i.putExtra("number",etNumber.getText().toString());
        startActivity(i);
    }
}
**MainActivity2.java:**
package com.example.experiment_4;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;

import android.os.Bundle;

import android.widget.TextView;


public class MainActivity2 extends AppCompatActivity
{

    TextView tv;

    @SuppressLint("SetTextI18n")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
        Bundle b = getIntent().getExtras();
        int no = Integer.parseInt(b.getString("number"));
        long f = 1;
        for (int i = no; i > 0; i--) {
            f = f * i;
        }
        tv = findViewById(R.id.tv);
        tv.setText("Factorial of " + no + " is " + f);
    }
}

**activity_main.xml:**

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/etNumber"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="50dp"
        android:hint="@string/Enter_the_number"
        android:importantForAutofill="no"
        android:inputType="number"
        tools:ignore="TextContrastCheck,TouchTargetSizeCheck" />

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:onClick="displayFactorial"
        android:text="factorial"
        tools:ignore="HardcodedText,VisualLintButtonSize" />
</LinearLayout>

**activity_main2.xml:**

<?xml version="1.0" encoding="utf-8"?>

<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
                
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="20dp"
    tools:context=".MainActivity2">

    <TextView
        android:id="@+id/tv"
        style="@style/TextAppearance.AppCompat.Large"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:text="@string/factorial_of_number_is" />
  
</RelativeLayout>


## OUTPUT:


![2023-06-08 (18)](https://github.com/santhoshkumar24263/Mobile-Application-Development/assets/127171952/0d6356a9-246c-4625-8755-176747a5d836)

![2023-06-08 (19)](https://github.com/santhoshkumar24263/Mobile-Application-Development/assets/127171952/be288f4d-0436-4197-a2cc-2ea61fad6616)



## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


