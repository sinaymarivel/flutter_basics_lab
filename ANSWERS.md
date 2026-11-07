# MariWeb Flutter Lab — Answers

**Student:** Marivel Charisse Sinay  
**Section:** ICLX3  
**Student ID:** 2023-1394

## 1. GitHub repository link
[https://github.com/sinaymarivel/flutter_basics_lab#flutter_basics_lab]

## 2. Last three Activity 2 Debug Console lines
The following are examples of the expected format only. Replace them with the actual last three lines copied from your VS Code Debug Console after tapping the tracker:
```text
build() called: 4 glasses
build() called: 5 glasses
build() called: 6 glasses
```

## 3. Activity experiment observations

### Activity 2 — changing the value outside setState()
When the glasses value is changed outside `setState()`, the Dart variable can change, but Flutter is not notified that the UI needs to rebuild. The displayed count and progress indicator may remain unchanged until another rebuild happens. Putting the update back inside `setState()` makes the screen refresh immediately.

### Activity 3 — removing Expanded
Without `Expanded`, a StatBox takes only the space its contents need instead of sharing the available row width equally. With four boxes, the row may look uneven or overflow if the total widths and gaps do not fit. `Expanded` distributes the available horizontal space among the boxes.

### Activity 5 — changing the button corner radius
Changing the elevated button corner radius from 8 to 20 makes the button corners more rounded. Since the style is set in `ThemeData`, it applies consistently to ElevatedButton widgets that use the theme.

## 4. Review questions

### 1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each from this lab.
A StatelessWidget does not keep data that changes while the app is running. Its UI is built from the values it receives. The ProfileCard in Activity 1 is an example. A StatefulWidget has a State object that can store changing data. The WaterTrackerPage in Activity 2 is an example because its glass count changes when the buttons are tapped.

### 2. Why is a StatefulWidget written as two classes? What does each class do?
It is written as two classes to separate the widget's configuration from its changing state. The StatefulWidget class creates the State object. The State class stores changing values and contains the build method and functions that update those values.

### 3. In Activity 2, what happened when you changed _glasses outside setState()? Why?
The value could change in the Dart code, but the screen did not automatically update. Flutter was not told that the state had changed because the update was outside `setState()`.

### 4. Looking at the Debug Console in Activity 2, when is build() called?
The `build()` method is called when Flutter first creates the screen and again when the widget needs to be rebuilt, such as after a state change made inside `setState()`.

### 5. Explain the main axis and the cross axis of a Row and of a Column.
For a Row, the main axis is horizontal and the cross axis is vertical. For a Column, the main axis is vertical and the cross axis is horizontal.

### 6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?
Without Expanded, the StatBox no longer shares the row's available width equally and instead takes the width its contents need. Expanded tells a child to take a share of the remaining available space.

### 7. Why do we use GridView.builder for the menu instead of a Column with many children?
GridView.builder arranges items in a grid and builds items as they are needed for display. It is suitable for a menu with multiple cards and supports scrolling. A Column simply places all children vertically and does not provide a grid layout by itself.

### 8. How do Stack and Positioned create the Best seller badge in Activity 4?
Stack places widgets on top of one another. The menu card content is placed in the stack, and Positioned places the Best seller badge at a specific location, in this case the top-left corner.

### 9. What is the difference between customizing with ThemeData and with a style on one widget? Give one example of each from Activity 5.
ThemeData sets styles that can be shared across the app, such as the elevated button theme and its corner radius. A style placed directly on one widget affects only that widget, such as giving an individual Text widget a specific font size.

### 10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the change reach MaterialApp?
The `_ThemeDemoAppState` object belonging to ThemeDemoApp holds the `_isDark` value. The switch calls `onDarkChanged`, which runs `_setDark` in the parent. That method updates `_isDark` inside `setState()`. MaterialApp then rebuilds and uses `themeMode` to select the light or dark theme.
