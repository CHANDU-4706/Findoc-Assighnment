# Flutter BLoC Picsum App

A simple Flutter application with **two screens** (Login and Home) using **BLoC/Cubit state management**,
**form validation**, and **API integration** with [Picsum](https://picsum.photos/).

- **Login Screen** with email & password validation.
- **Home Screen** fetches 10 images via `https://picsum.photos/v2/list?limit=10` and shows them in a vertical list.
- Titles use **Montserrat Semi-Bold**, descriptions use **Montserrat Regular** via `google_fonts`.
- Clean **repository + BLoC** architecture.

## Getting Started

```bash
# Ensure Flutter is installed and on PATH
flutter --version

# Fetch packages
flutter pub get

# Run the app
flutter run

# Build release APK
flutter build apk
```

The generated APK will be at:
`build/app/outputs/flutter-apk/app-release.apk`

## Project Structure

```
lib/
  main.dart
  app_router.dart
  core/
    validators.dart
  features/
    login/
      cubit/login_cubit.dart
      view/login_screen.dart
    photos/
      data/
        models/photo.dart
        photos_repository.dart
      bloc/photos_bloc.dart
      view/home_screen.dart
```

## Push to GitHub

```bash
git init
git add .
git commit -m "feat: initial Flutter BLoC Picsum app"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Notes

- This app does **not** perform a real login API call. Successful submission after validation navigates to Home.
- API integration requirement is fulfilled via the Picsum endpoint on the Home screen.
```
