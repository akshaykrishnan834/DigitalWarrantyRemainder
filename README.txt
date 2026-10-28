DIGITAL WARRANTY REMINDER - JAVA + SQLITE

PACKAGE:
com.example.digitalwarrantyreminder

PROJECT CONTENTS:
- MainActivity.java: Handles the screen, validates input and connects button clicks to database methods.
- DatabaseHelper.java: Extends SQLiteOpenHelper, creates the Warranty table, inserts warranty records and retrieves records.
- activity_main.xml: Defines the application user interface.
- AndroidManifest.xml: Declares the launcher activity.

SQLITE CONCEPTS USED (from the supplied Android SQLite notes):
- SQLiteOpenHelper
- onCreate()
- onUpgrade()
- getWritableDatabase()
- getReadableDatabase()
- ContentValues
- SQLiteDatabase.insert()
- rawQuery()
- Cursor
- cursor.moveToNext()
- cursor.getString()
- cursor.close()

HOW TO OPEN AND RUN:
1. Extract DigitalWarrantyReminder.zip.
2. Open Android Studio.
3. Select File > Open.
4. Select the extracted DigitalWarrantyReminder folder (the folder containing settings.gradle).
5. Wait for Gradle Sync to finish. If Android Studio asks to install Android SDK 35, allow it, or change compileSdk to an installed SDK version in app/build.gradle.
6. Create an Android emulator or connect an Android phone with USB debugging enabled.
7. Press the Run button.

HOW TO USE:
1. Enter a product name.
2. Enter purchase date in yyyy-MM-dd format, for example 2026-01-15.
3. Enter expiry date in yyyy-MM-dd format, for example 2027-01-15.
4. Press Save Warranty.
5. Press Display All Warranties to view saved records.

REMINDER BEHAVIOUR:
- More than 30 days remaining: Active status.
- 30 days or fewer remaining: Reminder warning.
- Expiry date is today: Expires today.
- Expiry date has passed: Expired.

The reminder status is calculated and shown when the app displays the warranty records. This project does not schedule background notifications; notification scheduling is not part of the supplied SQLite lesson.

DATABASE:
Database name: WarrantyDB
Table name: Warranty
Columns:
- id INTEGER PRIMARY KEY AUTOINCREMENT
- product_name TEXT NOT NULL
- purchase_date TEXT NOT NULL
- expiry_date TEXT NOT NULL

NOTE:
This is a beginner-friendly demonstration project based on the SQLiteOpenHelper example in the supplied learning material. It intentionally uses insert and SELECT operations, matching the lesson.
