# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## Algorithm

1. Start the application.
2. Create a new Android project in Android Studio.
3. Add an **EditText** for entering the website URL.
4. Add a **Button** labeled **"Navigate"**.
5. Initialize the EditText and Button in `MainActivity.java`.
6. Set an `OnClickListener` for the Navigate button.
7. Read the URL entered by the user from the EditText.
8. If the URL does not start with `http://` or `https://`, prepend `https://`.
9. Create an Implicit Intent using:
   ```java
   Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
   ```
10. Launch the browser using:
    ```java
    startActivity(intent);
    ```
11. The default web browser opens the specified website.
12. End the application.


## PROGRAM:
```
Program to print the text “Implicitintent”.
Developed by: GOKULNATH R
Registeration Number : 212224223001
```
## MainActivity.java
```java
package com.example.implictintent;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
        editText = (EditText) findViewById(R.id.editText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```
## Activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/btn"
        android:text="Search"
        android:onClick="search"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText" />


</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/37d764eb-47a9-4b08-a985-9c4b2b468df7" />


<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2f1b1d14-7ea2-4032-8dcd-6d37e264cd16" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


