Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors.
Note: Create button for colors and fonts while clicking color or font button should change

AIM:
To create an application that uses GUI Components with Fonts and Colors using Android Studio.

EQUIPMENTS REQUIRED:
Latest Version Android Studio

ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as GUI_Components and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

PROGRAM:
/*
Program to print the text “GUIcomponent”.
Developed by: SAM JOSHUA ML
Registeration Number :212221040142
*/
```
ACTIVITY_MAIN.XML:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="serif-monospace"
        android:text="@string/message"
        android:textAlignment="center"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.36" />

    <Button
        android:id="@+id/button2"
        android:layout_width="124dp"
        android:layout_height="63dp"
        android:text="@string/font"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.608" />

    <Button
        android:id="@+id/button"
        android:layout_width="129dp"
        android:layout_height="66dp"
        android:text="@string/color"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.757" />

</androidx.constraintlayout.widget.ConstraintLayout>
MAINACTIVITY.JAVA:
package com.example.gui_components;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.graphics.Color;
import android.graphics.Typeface;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    TextView textView;
    Float textSize,add=10.0f;
    Button colorButton;
    Button fontButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        textView = findViewById(R.id.textView);
        colorButton = findViewById(R.id.button);
        fontButton = findViewById(R.id.button2);

        colorButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                int randomColor = Color.rgb(
                        (int) (Math.random() * 256),
                        (int) (Math.random() * 256),
                        (int) (Math.random() * 256)
                );
                textView.setTextColor(randomColor);
            }
        });
        fontButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                textSize=textView.getTextSize();
                textSize=textSize+add;
                textView.setTextSize(textSize);
            }
        });
    }
}
```
OUTPUT
![image](https://github.com/samjoshua01/GUI-components/assets/152732933/aa192c94-50f8-4d0b-ad1b-d0bca9188bd4)
![image](https://github.com/samjoshua01/GUI-components/assets/152732933/a10842b9-1818-45ba-b8ef-a3c88239dec2)
![image](https://github.com/samjoshua01/GUI-components/assets/152732933/f933be70-2ba7-44a4-a7b3-37ef8a178602) ![image](https://github.com/samjoshua01/GUI-components/assets/152732933/14e56897-2db4-44ad-b203-8d12c8a62087) ![image](https://github.com/samjoshua01/GUI-components/assets/152732933/6745619d-edf3-4bcf-a044-75e60b6081f8)



    
RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.
