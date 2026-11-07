# MariWeb Flutter Lab — Step-by-step guide

## 1. Open the project
1. Extract this ZIP.
2. Open the extracted `ICLX3_SINAY_MARIVELCHARISSE` folder in VS Code (File > Open Folder).
3. Open Terminal > New Terminal.
4. Run `flutter doctor`. Confirm Flutter, Chrome and VS Code have check marks.
5. Run `flutter pub get`.
6. Run `flutter run -d chrome` (or press F5).

## 2. Select an activity
Open `lib/main.dart`. Change only the import filename to select an activity:
- `activity1_profile_card.dart`
- `activity2_water_tracker.dart`
- `activity3_weather_layout.dart`
- `activity4_cafe_menu.dart`
- `activity5_theme_components.dart`

Save, then press Ctrl+Shift+F5 to hot restart. Each activity's MaterialApp title is `MariWeb`.

## 3. Activity requirements already applied
- Activity 1: student name, email, phone row and spacing.
- Activity 2: goal is 6; personalized goal message.
- Activity 3: four stat boxes including Feels like.
- Activity 4: Matcha Latte and Pancakes added; one is marked best seller.
- Activity 5: UI/UX Design chip added; button radius changed from 8 to 20.

## 4. One item to verify/change
Activity 3 currently uses `Butuan City`, which is the example city in the manual. If this is not your hometown, replace it in `lib/activity3_weather_layout.dart`.

The profile program is set to BS Information Technology. Change it only if your actual program has a different official name.

## 5. Capture the required screenshots
Create/keep the `screenshots` folder. For each activity select it in `main.dart`, hot restart, and capture the Chrome app using Windows+Shift+S. Save:
1. `activity1.png` — profile and phone row.
2. `activity2_start.png` — tracker at 0 glasses.
3. `activity2_goal.png` — tracker at 6 glasses.
4. `activity3.png` — hometown and four stat boxes.
5. `activity4.png` — menu with the two extra items.
6. `activity5_light.png` — light mode with the Save SnackBar visible (press Save immediately before capture).
7. `activity5_dark.png` — dark mode enabled.

Do not use sample/blank images as screenshots; capture your actual running app so the title bar and UI are genuine.

## 6. Finish answers and GitHub
Open `ANSWERS.md`. Replace the GitHub placeholder after creating your repository, and replace the three sample Debug Console lines with the actual last three lines from your run. Read and personalize the answers/observations so you can explain them to your instructor.

## 7. Create GitHub repository
Create an empty public or instructor-approved repository named `flutter_basics_lab`. In the VS Code terminal, from this project folder, run (replace YOUR_USERNAME):
```
git init
git add .
git commit -m "Lab: Flutter widgets, layouts and UI components"
git branch -M main
git remote add origin https://github.com/sinaymarivel/flutter_basics_lab#flutter_basics_lab
git push -u origin main
```

## 8. Create the final ZIP
After all seven screenshots are in `screenshots`, run this PowerShell command from the project folder:
```
Compress-Archive -Path lib, pubspec.yaml, screenshots, ANSWERS.md -DestinationPath ICLX3_SINAY_MARIVELCHARISSE.zip -Force
```
The final ZIP should contain `lib/`, `pubspec.yaml`, `screenshots/` (seven real PNGs), and `ANSWERS.md`.
