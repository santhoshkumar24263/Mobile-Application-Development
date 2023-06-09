# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by:Santhosh Kumar B
Registeration Number :212221040146
*/
```
**MainActivity.java:**
package com.example.experiment_1;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.widget.Toast;

public class MainActivity extends AppCompatActivity 
{

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast.makeText(this, "onCreate Called", Toast.LENGTH_SHORT).show();
    }
    @Override
    protected void onRestart(){
        Toast.makeText(this, "onRestart Called", Toast.LENGTH_SHORT).show();
        super.onRestart();
    }
    @Override
    protected void onStart(){
        Toast.makeText(this, "onStart Called", Toast.LENGTH_SHORT).show();
        super.onStart();
    }
    @Override
    protected void onResume(){
        Toast.makeText(this, "onResume Called", Toast.LENGTH_SHORT).show();
        super.onResume();
    }
    @Override
    protected void onPause(){
        Toast.makeText(this, "onPause Called", Toast.LENGTH_SHORT).show();
        super.onPause();
    }
    @Override
    protected void onStop(){
        Toast.makeText(this, "onStop Called", Toast.LENGTH_SHORT).show();
        super.onStop();
    }
    @Override
    protected void onDestroy(){
        Toast.makeText(this, "onDestroy Called", Toast.LENGTH_SHORT).show();
        super.onDestroy();
    }
}

**activity_main.xml:**

<?xml version="1.0" encoding="utf-8"?>

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        android:textSize="20dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:ignore="SpUsage,TextSizeCheck" />
</androidx.constraintlayout.widget.ConstraintLayout>


## OUTPUT:


![2023-06-08 (1)](https://github.com/suryacse05/Mobile-Application-Development/assets/127171952/bb3e88f0-08c4-471b-b9af-0d47897be529)

![2023-06-08 (2)](https://github.com/suryacse05/Mobile-Application-Development/assets/127171952/de0df3c3-6693-4f96-b605-4ac5bb54ab30)

![2023-06-08 (5)](https://github.com/suryacse05/Mobile-Application-Development/assets/127171952/41519fd9-f9b0-4c3c-a904-ad79c6a5552f)

![2023-06-08 (7)](https://github.com/suryacse05/Mobile-Application-Development/assets/127171952/5393595f-ecb6-436d-a072-4e6c43d93491)

![2023-06-08 (3)](https://github.com/suryacse05/Mobile-Application-Development/assets/127171952/1ed170c9-0e97-4aaf-8c88-f7dc0dc9ec39)

![2023-06-08](https://github.com/suryacse05/Mobile-Application-Development/assets/127171952/2de6cb9c-6e27-45a4-b5f2-c72026b1890d)



## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
