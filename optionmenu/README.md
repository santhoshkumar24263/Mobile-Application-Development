# Ex.No:10 To create a option menu to display menu items.


## AIM:

To create a option menu to display menu items using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step1: Start the program

Step2: Create a new Android project in Android Studio or open an existing project.

Step3: Open the XML layout file for the activity where you want to display the options menu
(usually named activity_main.xml).

Step4: Add a Toolbar widget to the layout file to act as the action bar for the activity.

Step5: In the Java file for the activity (usually named MainActivity.java):

Step6: Override the onCreateOptionsMenu() method to inflate the menu resource file and
display the options menu.

Step7: Implement the onOptionsItemSelected() method to handle the selected menu item's
actions.

Step8: Create an XML file in the res/menu directory to define the menu items.

Step9: Specify the menu items in the XML file, including their IDs, titles, and other
attributes.

Step10: Handle the selected menu item's actions in the onOptionsItemSelected() method
based on its ID.

Step11: Customize the menu items and their behavior as per your requirements.

Step12: Run the Android application to see the options menu displayed in the activity's action
bar.

Step13: Implement the desired actions for each menu item by adding the necessary code
within the onOptionsItemSelected() method.

Step14: End the program


## PROGRAM:
```
/*
Program to print the text “optionmenu”.
Developed by:Santhosh Kumar B
Registeration Number :212221040146
*/
```
**MainActivity.java:**
package com.example.experiment_9;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;

import android.os.Bundle;

import android.widget.Button;

import android.widget.EditText;

import android.widget.TextView;

import android.widget.Toast;

public class MainActivity extends AppCompatActivity
{

    Button btnadd,btnsubs,btnmult,btndiv;
    EditText txt1,txt2;
    TextView result;
    @SuppressLint("SetTextI18n")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        btnadd=findViewById(R.id.btnadd);
        btnsubs=findViewById(R.id.btnsubs);
        btndiv=findViewById(R.id.btndiv);
        btnmult=findViewById(R.id.btnmult);
        txt1=findViewById(R.id.txt1);
        txt2=findViewById(R.id.txt2);
        result=findViewById(R.id.result);
        btnadd.setOnClickListener(view -> {
            if (txt1.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            } else if (txt2.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            }
            else {
                float a, b, c;
                a = Float.parseFloat(txt1.getText().toString());
                b = Float.parseFloat(txt2.getText().toString());
                c = a + b; // Using Third Variable To Store Output Value
                result.setText("The Addition Result Is " + c);
            }
        });
        btnsubs.setOnClickListener(view -> {
            if (txt1.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            } else if (txt2.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            }
            else {
                float a, b, c;
                a = Float.parseFloat(txt1.getText().toString());
                b = Float.parseFloat(txt2.getText().toString());
                c = a - b; // Using Third Variable To Store Output Value
                result.setText("The Subtraction Result Is " + c);
            }
        });
        btnmult.setOnClickListener(view -> {
            if (txt1.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            } else if (txt2.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            }
            else {
                float a, b, c;
                a = Float.parseFloat(txt1.getText().toString());
                b = Float.parseFloat(txt2.getText().toString());
                c = a*b; // Using Third Variable To Store Output Value
                result.setText("The Multiplication Result Is " + c);
            }
        });
        btndiv.setOnClickListener(view -> {
            // Checking Input First Is Blank Or Not
            if (txt1.getText().toString().equals("")) {
                // Showing Toast (Message)
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            } else if (txt2.getText().toString().equals("")) {
                Toast.makeText(MainActivity.this, "Please Enter Number",
                        Toast.LENGTH_SHORT).show();
            }
            else {
                float a, b, c;
                a = Float.parseFloat(txt1.getText().toString());
                b = Float.parseFloat(txt2.getText().toString());
                c = a/b; // Using Third Variable To Store Output Value
                result.setText("The Division Result Is " + c);
            }
        });
    }
}

**activity_main.xml:**

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
              
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:orientation="vertical">
    <ImageView
        android:id="@+id/imageView"
        android:layout_width="match_parent"
        android:layout_height="111dp"
        android:layout_marginTop="25dp"
        app:srcCompat="@drawable/img"
        tools:ignore="ContentDescription" />

    <EditText
        android:id="@+id/txt1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="20dp"
        android:layout_marginRight="20dp"
        android:ems="10"
        android:hint="First Number"
        android:inputType="numberDecimal"
        tools:ignore="Autofill,HardcodedText,SpeakableTextPresentCheck,TouchTargetSizeCheck,TextContrastCheck,VisualLintTextFieldSize" />

    <EditText
        android:id="@+id/txt2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="20dp"
        android:layout_marginRight="20dp"
        android:ems="10"
        android:hint="Second Number"
        android:inputType="numberDecimal"
        tools:ignore="Autofill,HardcodedText,SpeakableTextPresentCheck,TouchTargetSizeCheck,TextContrastCheck,VisualLintTextFieldSize" />
    <Button
        android:id="@+id/btnadd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="20dp"
        android:layout_marginRight="20dp"
        android:text="Add"
        tools:ignore="HardcodedText,VisualLintButtonSize" />
    <Button
        android:id="@+id/btnsubs"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="20dp"
        android:layout_marginRight="20dp"
        android:text="Subtract"
        tools:ignore="HardcodedText,VisualLintButtonSize" />
    <Button
        android:id="@+id/btndiv"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="20dp"
        android:layout_marginRight="20dp"
        android:text="Divide"
        tools:ignore="HardcodedText,VisualLintButtonSize" />
    <Button
        android:id="@+id/btnmult"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="20dp"
        android:layout_marginRight="20dp"
        android:text="Multiply"
        tools:ignore="HardcodedText,VisualLintButtonSize" />
    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginTop="25dp"
        android:layout_marginRight="20dp" />
  
</LinearLayout>


## OUTPUT:



![Screenshot 2023-06-09 151947](https://github.com/santhoshkumar24263/Mobile-Application-Development/assets/127171952/bcda46ea-e1ef-486f-b4a3-45f912c07b1d)


## RESULT
Thus a Simple Android Application to create a option menu to display menu items using Android Studio is developed and executed successfully.


