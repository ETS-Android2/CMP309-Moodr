# CMP309Coursework - Mood Calendar

A Mood Calendar application I made for Android Dev at Abertay University

## App Outline

- A Mood Calendar and well-being app for Android
- Built with the intent of allowing users to keep track of their mood, and improve it, should the need arise
- Allows for storing of mood (represented by a number 1-5), and three good things that happened on that day
  - These must have a mood, a date (generated by the backend) and a body of text, be it three separate things or one main diary entry
- Send notifications to the user reminding them to input a diary entry
  - Should be modifiable based on time (so you can set it to remind you at specific times)
- Store data on users locally and provide analysis of the last week, month, and year in their mood
- Habit Former (walks, meditation, and so on) with timer and special notification

## Functional Requirements

1. Allow the user to input how they're feeling to a database object linked to the date
   1. Five buttons representing a sliding scale of happiness, from 1 = sad to 5 = happy
   2. Title text entry to give an overview of what happened
   3. Diary text entry field so the user can talk about what happened to them
      1. Maybe add tags? See how I feel and leave that for later depending
2. Allow the user to input three good things that happened to them today
   1. Talk about the studies that mention how good this is
3. Allow the user to create "Habits", or little things they do every day at a certain time, e.g. meditation or going for a walk
   1. Maybe add timer to this in the app, also?
4. Create a settings view for the user to edit their preferences
5. Store statistics for how the user has felt over the last few days, weeks, and months
   1. Seen as how all the data used will be collected on a single user we can merge all of the database objects together based on date and do statistical analysis herein
   2. How the user is feeling
   3. The text they inputted
   4. Three things that made them happy that day
   5. How they're doing in their habits
6. A splash screen
   1. Have some information about how to use the app here
   2. What everything does
   3. Will need a logo for this, also
7. Add more possibly depending on requirements

## Non-Functional Requirements

1. Responsiveness
   1. Asynchronous operations for transactions
   2. zero hangs
2. Good error handling
3. Restore user states
4. Model View Controller pattern
5. Attractiveness
   1. Probably Material UI

## How Each Assessment Criteria Will Be Met

### Principles of Object-Oriented programming

This requirement will be met by virtue of developing the app in Java, a fundamentally Object-Oriented programming language. 

### At least 2 Activities and communication between Activities and returning a result from Activity

The application as planned currently has 5 sets of activities. The primary place communication between activities will be achieved is in the TGT and Diary/Calendar input's relationship with the "Reports" section, where data will be sent between the two to facilitate the functionality therein. The Settings Activity will also return results, allowing for the user to change the theme and customise notification times where relevant

###  At least 3 screens/pages showing different aspects of the app and utilising multiple layouts, views and/or UI widgets. These can include Activities, Tabs, Fragments, Navigation Drawer menus, pop-up dialogues, webviews, etc.

The app primarily uses activities for navigation, there is also the use of fragments in a tabbed activity, a time widget, pop up dialogues to allow users to delete items, etc.

### Appropriate application lifecycle, including correct navigation through Activity stack, handling of device orientation changes and correct use of lifecycle callback functions for registering/unregistering receivers and listeners, saving/restoring data, etc.

This requirement will be met by making sure that the app state is restored when coming back into view to the user after being closed.

The second two can just be met through the use of good programming practice.

### Appropriate use of multi-threading for file saving/loading, data upload/download and other resource-intensive operations

Ensure all operations are done asynchronously, primarily concerning reading from the database, i.e. it should never cause a hang. 

**NOTE** Android View objects are not thread-safe and therefore UI elements should never be multithreaded in Android, therefore the only place that can be multithreaded is in the database etc.

### Using at least one of the data storage methods used in the module

The use of SQLite satisfies this requirement

### Using at least one of the native Android API features OR Mobile networking technologies

Sending the user a notification will satisfy this.

## App Hierarchy

\[Insert Image Here\]

## Other stuff

\[Insert as and when required\]

## References

- Abdi, J. (2019) ‘Answer to “How to show a notification everyday at a certain time even when the app is closed?”’, Stack Overflow. Available at: https://stackoverflow.com/a/55910596/12207605 (Accessed: 3 May 2022).
- Android - Time Picker (no date). Available at: https://www.tutorialspoint.com/android/android_timepicker_control.htm (Accessed: 23 April 2022).
- ‘Android SQLite Database Example Tutorial’ (2015) JournalDev, 21 October. Available at: https://www.journaldev.com/9438/android-sqlite-database-example-tutorial (Accessed: 17 April 2022).
- Android SQLite ListView with Examples - Tutlane (no date). Available at: https://www.tutlane.com/tutorial/android/android-sqlite-listview-with-examples (Accessed: 9 May 2022).
- Dekanski, D. (2021) BottomNavigationView switching between activities. Available at: https://github.com/ddekanski/BottomNavigationViewBetweenActivities (Accessed: 12 April 2022).
- Displaying dialogs with DialogFragment (no date) Android Developers. Available at: https://developer.android.com/guide/fragments/dialogs (Accessed: 25 April 2022).
- Jha, A. (2016) ‘Answer to “How to Store an int in SharedPreferences”’, Stack Overflow. Available at: https://stackoverflow.com/a/38099562/12207605 (Accessed: 11 May 2022).
- Kuzubasioglu, E. (2016) ‘How to create a day counter for android application?’, Stack Overflow. Available at: https://stackoverflow.com/q/39179974/12207605 (Accessed: 17 April 2022).
- major (2017) ‘Displaying ALL data from sqlite database into listview in tabbed activity’, Stack Overflow. Available at: https://stackoverflow.com/q/47954066/12207605 (Accessed: 17 April 2022).
- Ochieng, C. (2016) Android Tabbed Data Ep.02 : ListView- Swipe Fragments SQLite CRUD. Available at: https://www.youtube.com/watch?v=O7noFYLxP14 (Accessed: 9 May 2022).
- Patel, V. (2016) ‘Answer to “How to set confirmation delete message (AlertDialog) for my list view for android studio”’, Stack Overflow. Available at: https://stackoverflow.com/a/36106306/12207605 (Accessed: 27 April 2022).
- Pixel cow image for game assets vector image on VectorStock (no date) VectorStock. Available at: https://www.vectorstock.com/royalty-free-vector/pixel-cow-image-for-game-assets-vector-38165012 (Accessed: 22 April 2022).
- Rippstein-Leuenberger, K. et al. (2017) ‘A qualitative analysis of the Three Good Things intervention in healthcare workers’, BMJ Open, 7(5), p. e015826. doi:10.1136/bmjopen-2017-015826.
- Sanath14 (2021) Sanath14/to-do-list-using-sqlite. Available at: https://github.com/Sanath14/to-do-list-using-sqlite (Accessed: 13 April 2022).
- SharedPreferences  |  Android Developers (no date). Available at: https://developer.android.com/reference/android/content/SharedPreferences (Accessed: 17 April 2022).
- SVG to Vector Drawable Converter – Convert SVG, PNG, JPEG, GIF images to Android VectorDrawable XML resource files online (no date). Available at: https://svg2vector.com/ (Accessed: 22 April 2022).
- SwitchPreferenceCompat  |  Android Developers (no date). Available at: https://developer.android.com/reference/androidx/preference/SwitchPreferenceCompat (Accessed: 17 April 2022).
- Taioli, F. (2016) ‘Answer to “How to create a day counter for android application?”’, Stack Overflow. Available at: https://stackoverflow.com/a/39180033/12207605 (Accessed: 17 April 2022).
- ViewModel | Android Developers (no date). Available at: https://developer.android.com/reference/android/arch/lifecycle/ViewModel (Accessed: 14 May 2022).
- Vujovic, F. (2016) Daily Repeating Local Notification In Android. Available at: https://www.youtube.com/watch?v=1fV9NmvxXJo (Accessed: 12 May 2022).
- Yousaf (2017) ‘Answer to “Displaying ALL data from sqlite database into listview in tabbed activity”’, Stack Overflow. Available at: https://stackoverflow.com/a/47954360/12207605 (Accessed: 17 April 2022).
