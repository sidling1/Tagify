# Tagify 💬

Tagify enables the user to create and manage groups with ease. It lets the user find the right set of people and communicate relevant information with them.
- After creating an account, users can assign themselves tags, for e.g. appdev, rajasthan, burger, etc.
- Say we want to address everyone who is in Rajasthan and likes Burger or is in Assam and likes Fish, then we can simply create a group with this logic: `(rajasthan AND burger) OR (assam AND fish)` which is equivalent to `(rajasthan & burger) | (assam & fish)` and a group with those people will automatically be made!
- To enter the logic for a group, we are using a bunch of buckets, there can be any number of buckets, and each bucket can contain any number of tags. The tags inside a bucket are `AND`ed, and then the buckets are `OR`ed together.

## Setting up the project in your local environment💻

<p align="center">
    <img src="https://user-images.githubusercontent.com/74055102/141175363-4c00515a-2658-475e-b510-394110d43ec5.png" height=400/>
</p>

1. [Fork](https://github.com/sidling1/Tagify/fork) this repository.
2. Clone the **forked** repository:
```
git clone https://github.com/<your username>/Tagify
cd Tagify
```
3. Add a remote to the upstream repository:
```
# Typing the command below should show you only 1 remote named origin with the URL of your forked repository
git remote -v
# Adding a remote for the upstream repository
git remote add upstream [url]
```
4. Get [Flutter](https://docs.flutter.dev/get-started/install) and [Firebase CLI](https://firebase.google.com/docs/cli?authuser=0&hl=en#install_the_firebase_cli) if you don't already have them.
5. Run `flutter pub get` to get the dependencies.
6. If you have not yet logged into `Firebase CLI` and activate `FlutterFire CLI` globally:
```
firebase login
dart pub global activate flutterfire_cli
```
7. Create a new project on [Firebase Console](https://console.firebase.google.com/), activate Google Sign In, and activate Firebase Firestore in **test mode**.
8. Configure your flutter app with the newly created project on firebase console:
```
flutterfire configure
```

This automatically registers your per-platform apps with Firebase and adds a `lib/firebase_options.dart` configuration file to your Flutter project.

9. Finally, run the app:
```
flutter run
```