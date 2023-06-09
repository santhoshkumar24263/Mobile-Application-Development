# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step1:Create a new Android Studio project.

Step2:Open the layout file "activity_main.xml".

Step3:Add a container layout to hold the gallery images (e.g., GridLayout, RecyclerView, or
ViewPager).

Step4:Within the container layout, add ImageView elements to display the images. You can
set the image source using the android:src attribute or programmatically in the code.

Step5:If using a GridLayout, specify the number of columns using the android:columnCount
attribute.

Step6:Customize the layout and appearance of the ImageView elements as desired.

Step7:Add any necessary attributes or listeners to handle user interactions, such as clicks on
the images.

Step8:Optionally, create a data source to store the images (e.g., a list or an array of image
references).

Step9:Bind the data source to the gallery control to populate the images dynamically.

Step10:Implement any additional functionality, such as zooming, sliding, or image
transitions, if desired.

Step11:Build and run the application to see the gallery control displaying the images.


## PROGRAM:
```
/*
Program to print the text “GalleryControl”.
Developed by:Santhosh Kumar B
Registeration Number :212221040146
*/
```

**MainActivity.java:**

package com.example.experiment_8;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.widget.Gallery;

import android.widget.ImageView;

public class MainActivity extends AppCompatActivity 
{

    Gallery simpleGallery;
    CustomizedGalleryAdapter customGalleryAdapter;
    ImageView selectedImageView;
    int[] images = {
            R.drawable.img, R.drawable.img_1, R.drawable.img_7,
            R.drawable.img_2, R.drawable.img_8,
            R.drawable.img_3, R.drawable.img_4, R.drawable.img_5, R.drawable.img_6,
            R.drawable.img_3,
            R.drawable.img_4, R.drawable.img, R.drawable.img_1, R.drawable.img_7,
            R.drawable.img_2, R.drawable.img_5,};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
        selectedImageView = (ImageView) findViewById(R.id.imageView);
        simpleGallery.setAdapter(customGalleryAdapter);
        simpleGallery.setOnItemClickListener((parent, view, position, id) -> {
            selectedImageView.setImageResource(images[position]);
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
        android:layout_width="fill_parent"
        android:layout_height="288dp"
        android:scaleType="fitXY" />
    <Gallery
        android:id="@+id/languagesGallery"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="100dp"
        android:animationDuration="2000"
        android:padding="10dp"
        android:spacing="5dp"
        android:unselectedAlpha="50" />
</LinearLayout>


## OUTPUT

![Screenshot 2023-06-09 143759](https://github.com/santhoshkumar24263/Mobile-Application-Development/assets/127171952/9d326fe1-4b20-483f-9b46-5f9003843f9d)



## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.


