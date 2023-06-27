Ex.No:6 Design an android application Send SMS using Intent.

AIM:

To create and design an android application Send SMS using Intent using Android Studio.

EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

PROGRAM:

/*

Program to create and design an android application Send SMS using Intent.

Developed by: Arun Karthik.V

Registeration Number : 212221040018

*/

activity_main.xml:

<?xml version="1.0" encoding="utf-8"?>	

<androidx.constraintlayout.widget.ConstraintLayout 

xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:app="http://schemas.android.com/apk/res-auto"

xmlns:tools="http://schemas.android.com/tools" 

android:layout_width="match_parent"
 
android:layout_height="match_parent" tools:context=".MainActivity">

<EditText
  
android:id="@+id/editTextTextPersonName" 

android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:ems="10" android:inputType="textPersonName" 

android:text="Message" 

app:layout_constraintBottom_toBottomOf="parent" 

app:layout_constraintEnd_toEndOf="parent"

app:layout_constraintHorizontal_bias="0.497" 

app:layout_constraintStart_toStartOf="parent" 

app:layout_constraintTop_toTopOf="parent" 

app:layout_constraintVertical_bias="0.351" />

<Button
  
android:id="@+id/button" 

android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:text="Send"

app:layout_constraintBottom_toBottomOf="parent"

app:layout_constraintEnd_toEndOf="parent" 

app:layout_constraintHorizontal_bias="0.498"

app:layout_constraintStart_toStartOf="parent"

app:layout_constraintTop_toBottomOf="@+id/editTextTextPersonName" 

app:layout_constraintVertical_bias="0.186" />

</androidx.constraintlayout.widget.ConstraintLayout>

activity_main2.xml:

<?xml version="1.0" encoding="utf-8"?>	

<androidx.constraintlayout.widget.ConstraintLayout 

xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:app="http://schemas.android.com/apk/res-auto" 

xmlns:tools="http://schemas.android.com/tools" 

android:layout_width="match_parent"

android:layout_height="match_parent" 

tools:context=".MainActivity2">

<TextView
  
android:id="@+id/textView" 

android:layout_width="wrap_content" 

android:layout_height="wrap_content" 

android:text="TextView" 

app:layout_constraintBottom_toBottomOf="parent" 

app:layout_constraintEnd_toEndOf="parent" 

app:layout_constraintHorizontal_bias="0.47" 

app:layout_constraintStart_toStartOf="parent"

app:layout_constraintTop_toTopOf="parent" 

app:layout_constraintVertical_bias="0.45" />

</androidx.constraintlayout.widget.ConstraintLayout>

MainActivity.java:-

package com.example.exp_06;	 

import android.content.Intent; 

import android.os.Bundle; 

import android.widget.Button; 

import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity; 

public class MainActivity extends AppCompatActivity {

// define the variable Button send_button; 

EditText send_text;

@Override

protected void onCreate(Bundle savedInstanceState) { 

super.onCreate(savedInstanceState); 

setContentView(R.layout.activity_main);

send_button = findViewById(R.id.button);

send_text = findViewById(R.id.editTextTextPersonName);

send_button.setOnClickListener(v -> {

String str = send_text.getText().toString();

Intent intent = new Intent(getApplicationContext(),

MainActivity2.class);

intent.putExtra("message_key", str);

startActivity(intent);

});

  }
  
}

MainActivity2.java:-

package com.example.exp_06;

import android.content.Intent;

import android.os.Bundle; 

import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity2 extends AppCompatActivity

{

TextView receiver_msg;

@Override

protected void onCreate(Bundle savedInstanceState)

{

super.onCreate(savedInstanceState); 

setContentView(R.layout.activity_main2);

receiver_msg = findViewById(R.id.textView);

// create the get Intent object 

Intent intent = getIntent();

// receive the value by getStringExtra() method and

// key must be same which is send by first activity 

String str = intent.getStringExtra("message_key");

// display the string into textView

receiver_msg.setText(str);

}

}

OUTPUT:

![image](https://github.com/Karthik2821/SMSintent/assets/134921933/47c296c4-38f2-41e0-aad2-c6efb4115e4c)

![image](https://github.com/Karthik2821/SMSintent/assets/134921933/a025db74-3eac-4618-9962-34708680bcdb)

![image](https://github.com/Karthik2821/SMSintent/assets/134921933/a83e7db0-5b05-4231-b5eb-17a1dd60e2b0)

RESULT:

Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.



















