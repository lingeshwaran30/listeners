# 5. Develop an Android Application Demonstrating Event Handling Using Listeners (OnClick, OnLongClick, etc.)

[← Back to Index](README.md)

## Project Name
`EventHandlingDemo`

## Aim
To develop an Android application demonstrating event handling using `OnClickListener` and `OnLongClickListener`.

## 1. File Name: `activity_main.xml`

**File Path:** `app/src/main/res/layout/activity_main.xml`

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <Button
        android:id="@+id/btnClick"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Click Me" />

    <Button
        android:id="@+id/btnLongClick"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Long Press Me"
        android:layout_marginTop="20dp" />

</LinearLayout>
```

## 2. File Name: `MainActivity.java`

**File Path:** `app/src/main/java/com/example/eventhandlingdemo/MainActivity.java`

```java
package com.example.eventhandlingdemo;

import android.os.Bundle;
import android.widget.Button;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    Button btnClick, btnLongClick;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        btnClick = findViewById(R.id.btnClick);
        btnLongClick = findViewById(R.id.btnLongClick);

        // OnClickListener
        btnClick.setOnClickListener(v -> {
            Toast.makeText(
                    MainActivity.this,
                    "Button Clicked",
                    Toast.LENGTH_SHORT
            ).show();
        });

        // OnLongClickListener
        btnLongClick.setOnLongClickListener(v -> {
            Toast.makeText(
                    MainActivity.this,
                    "Button Long Pressed",
                    Toast.LENGTH_SHORT
            ).show();

            return true;
        });
    }
}
```

**Important:** Ensure that the package name `com.example.eventhandlingdemo` matches your Android Studio project's package name.

## 3. Explanation

### OnClickListener
- `OnClickListener` handles a normal click on a view.
- When the user clicks the **Click Me** button, a Toast message displays **Button Clicked**.
- The listener is registered using `setOnClickListener()`.

### OnLongClickListener
- `OnLongClickListener` handles a long press on a view.
- When the user presses and holds the **Long Press Me** button, a Toast message displays **Button Long Pressed**.
- The listener is registered using `setOnLongClickListener()`.
- Returning `true` indicates that the long-click event has been handled.

## 4. Expected Output

1. The application displays two buttons: **Click Me** and **Long Press Me**.
2. Clicking **Click Me** displays the Toast message `Button Clicked`.
3. Pressing and holding **Long Press Me** displays the Toast message `Button Long Pressed`.

## 5. Result

Thus, an Android application demonstrating event handling using `OnClickListener` and `OnLongClickListener` was developed successfully.

## 6. Upload the Project to GitHub

1. Open your project folder.
2. Create or update the `README.md` file with this content.
3. Save the file.
4. Open your GitHub repository.
5. Commit and push your changes.

### Git Commands

```bash
git add README.md
git commit -m "Add Event Handling using Listeners practical"
git push
```
