# Hello-World------android

java.code

package com.example.hearterfly.firstcode;

import android.app.Activity;
import android.os.Bundle;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;
import android.widget.Toast;



public class MainActivity extends Activity {

    private Button button;

	@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        button = (Button) findViewById(R.id.button1);
        button.setOnClickListener(new MyOnClickListener());
    }
	
	private class MyOnClickListener implements OnClickListener {

		@Override
		public void onClick(View arg0) {
			// TODO Auto-generated method stub
			Toast.makeText(MainActivity.this, "Hello world", Toast.LENGTH_SHORT).show();
		}
		
	}

}


xml.code

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical" >

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/Girl" />
    <Button 
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/Button1"
        android:textColor="#ffff00"
        />

</LinearLayout>


strings.code

<?xml version="1.0" encoding="utf-8"?>
<resources>

    <string name="app_name">FirstCode</string>
    <string name="Girl">I Love the girl that is beautiful and kind-hearted !</string>
    <string name="action_settings">Settings</string>
	<string name="Button1">OnClick</string>
</resources>



