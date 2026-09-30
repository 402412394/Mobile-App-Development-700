# Mobile-App-Development-700

Smart Pantry Manager

## About the app

Smart Pantry Manager is an offline Android app I developed to make it easier to keep track of pantry ingredients and find recipes that can be made with what is available. Pantry items and the app's starter recipes are saved locally in SQLite, so the app does not need an internet connection to work.

The recipe suggestions are strict: a recipe only appears if the pantry has every ingredient it lists, with a quantity of at least one. Ingredient names are checked without considering capital letters, extra spaces, or common singular and plural endings. Quantities are compared as numbers, but units are not converted. For example, the app does not treat grams and kilograms as equivalent, so consistent units should be used for each ingredient.

## Why SQLite?

I chose SQLite because pantry information is personal data that can be kept on the device. It works offline, and Android includes `SQLiteOpenHelper` for creating and managing a local database. Users can add, view, update, and delete pantry items, and their records are still there after the app is closed.

## Main features

- **Pantry:** View the saved ingredients. Tap an item to edit it, or long-press it to delete it.
- **Add or edit ingredients:** Enter a name and positive quantity. A unit can also be added, but it is optional.
- **Suggested recipes:** See recipes that match all their listed ingredients, or an empty-state message if none match.
- **Recipe details:** View the ingredients and preparation steps for a recipe.
- **Settings:** Turn the expiry-reminder preference on or off. This is a demonstration setting only; the app does not currently store expiry dates or schedule notifications.

The project includes 18 starter recipes. Recipe quantities are not currently stored, and the app does not convert between units. These would be useful improvements for a future version.

## Opening and running the project

1. Install Android Studio, Android SDK 34, and JDK 17.
2. Open this folder in Android Studio as an existing Gradle project and let Gradle sync.
3. Create an emulator running API 23 or later, or connect an Android device with USB debugging enabled.
4. Select the `app` run configuration and run the project.
