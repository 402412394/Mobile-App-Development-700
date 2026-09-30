# Smart Pantry Manager

## Android project and home screen

I set up the Android project and added the files needed to build and run it. The app currently opens to a basic home screen, which I’ll build on as I add more features. This includes the Gradle 8.13 wrapper, project and app Gradle files, the manifest, and the `MainActivity` class.

## SQLite database and pantry table

I added `PantryDb`, a helper class that extends Android’s `SQLiteOpenHelper`. It creates and manages a local SQLite database, including the table used to store pantry items. The class also contains the recipe data and database methods supplied in the completed reference helper.

The `PantryDb.java` file is included as reference material for this stage. Its implementation was copied from the completed reference project, so I have identified that here rather than presenting it as code I wrote from scratch.
