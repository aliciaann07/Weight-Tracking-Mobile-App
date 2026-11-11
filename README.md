# Weight Tracking Mobile App

## Overview

The Weight Tracking Mobile App is an Android application developed using Java, XML, and SQLite. The application allows users to manage their weight history, record workout activity, and track their fitness progress through a centralized interface.

Originally developed for CS 360, the application was later enhanced as part of my computer science capstone. The enhancement focused on expanding the application's functionality by introducing workout history tracking and integrating additional database operations.

This project demonstrates my experience with Android application development, database integration, user interface design, input validation, and software engineering principles.

## Features

### User Account Management
- Create a user account and log in using registered credentials.
- Store and retrieve account information through SQLite.
- Associate weight and workout records with individual users.

### Weight History Tracking
- Record weight entries with dates and weight values.
- View previously recorded weight history.
- Add, update, and delete weight records.
- Store weight information in a local SQLite database.

### Workout History Tracking
- Record workout dates, exercise names, durations, and calories burned.
- View workout history in a table.
- Add, update, and delete workout records.
- Validate user input before saving workout information.
- Store workout records in SQLite for later retrieval.

### SMS Notification Settings
- Configure a goal weight and phone number.
- Enable SMS functionality with the required Android permissions.
- Send a test SMS message.
- Save notification preferences in SQLite.

## Technologies Used

| Technology | Purpose |
|---|---|
| Java | Application functionality and business logic |
| Android Studio | Development environment |
| XML | User interface layouts and resources |
| SQLite | Local database storage |
| SQLiteOpenHelper | Database creation, management, and CRUD operations |
| Android SDK | Application components, navigation, and SMS functionality |
| Gradle | Build configuration and dependency management |

## Application Architecture

The application separates its user interface components from database management responsibilities.

**User Interface**

Android activities manage user interactions, navigation, input validation, and the display of weight and workout information. XML layout files define the visual structure of each screen.

**Database Management**

The `DatabaseHelper` class extends `SQLiteOpenHelper` and manages database creation, upgrades, and data operations.

The database contains four tables:

- `users`: Stores user account information.
- `weights`: Stores weight history records associated with users.
- `workouts`: Stores workout activity, including exercise names, durations, and calories burned.
- `settings`: Stores goal weights, phone numbers, and SMS notification preferences.

The activities communicate directly with the database helper to perform the necessary operations.

## Software Engineering Enhancement

The primary enhancement to the original application was the implementation of workout history tracking.

This required expanding the existing SQLite database structure, creating a new Android activity and XML layout, and implementing methods to add, retrieve, update, and delete workout records.

The enhancement also required maintaining consistency with the application's existing navigation and database functionality.

Through this process, I applied software design principles to extend an existing application while preserving its original functionality.

## Project Structure

```text
app/
└── src/
    ├── main/
    │   ├── java/
    │   │   └── com/example/alicianicholson_weighttrackingmobileapp/
    │   │       ├── DatabaseHelper.java
    │   │       ├── LoginActivity.java
    │   │       ├── WeightHistoryActivity.java
    │   │       ├── WorkoutHistoryActivity.java
    │   │       └── SmsNotificationsActivity.java
    │   ├── res/
    │   │   ├── layout/
    │   │   ├── drawable/
    │   │   └── values/
    │   └── AndroidManifest.xml
    ├── test/
    └── androidTest/
```

## Getting Started

### Requirements

- Android Studio
- Android SDK 34 or higher
- Java 11 compatibility
- Android emulator or compatible physical device running Android 14 (API 34) or higher

### Installation

1. Clone or download the repository.
2. Open Android Studio.
3. Select **Open** and navigate to the project's root directory.
4. Allow Gradle to synchronize the project dependencies.
5. Configure an Android emulator or connect a compatible Android device.
6. Build and run the application.

**Note:** SMS functionality requires appropriate permissions and a device or emulator environment capable of supporting SMS operations.

## Testing and Validation

The project includes standard Android unit test and instrumented test files.

The application code also includes input validation and error handling for account management, weight entries, workout records, and SMS settings.

Further automated testing and validation would be beneficial before considering the application production-ready.

## Future Improvements

Potential future enhancements include:

- Implementing secure password hashing and stronger authentication.
- Improving database migration handling to preserve existing user data.
- Adding charts to visualize weight and workout progress.
- Expanding workout tracking and fitness goal features.
- Improving accessibility and responsive layouts.
- Adding automated tests for database operations and application functionality.

## Project Background

This application began as a mobile development project for CS 360 and was enhanced during my computer science capstone.

The enhancement provided an opportunity to work with an existing codebase, extend database functionality, implement additional user-facing features, and apply software engineering practices.

The project reflects my experience designing, implementing, and improving an Android application independently.

## Author

**Alicia Nicholson**

Computer Science | Software Engineering | Android Application Development
