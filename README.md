RU Fossil Park

Overview

RU Fossil Park is a Flutter application project designed to provide
information about fossils associated with the RU (Rowan University)
Fossil Park. The current project contains the basic application shell,
including a splash screen, a home page, and planned navigation to fossil
categories.

The project is currently in an incomplete/template state. Several
referenced screens, image assets, and a package dependency are missing
from the submitted source, so the application will require additional
work before it can run successfully as intended.

Project Goals

The application is structured around the following sections:

About RU Fossil Park --- information about the fossil park.

Invertebrates --- information about invertebrate fossils.

Vertebrates --- information about vertebrate fossils.

Non-Fossils --- information about non-fossil material.

Splash Screen --- an introductory screen displayed when the
application starts.

Technology

Framework: Flutter

Language: Dart

Minimum Dart SDK: 3.3.3

Target SDK range: < 4.0.0

Application version: 1.0.0+1

Platforms scaffolded: Android, iOS, Linux, macOS, Web, and
Windows

UI: Flutter Material widgets

Project Structure

final_dino1/
├── android/                 # Android platform configuration
├── ios/                     # iOS platform configuration
├── linux/                   # Linux platform configuration
├── macos/                   # macOS platform configuration
├── web/                     # Web platform configuration
├── windows/                 # Windows platform configuration
├── lib/
│   ├── main.dart            # Application entry point and splash screen
│   ├── aftersplash.dart     # Main MaterialApp and named routes
│   └── homepage.dart        # RU Fossil Park home screen
├── test/
│   └── widget_test.dart     # Flutter widget test template
├── pubspec.yaml             # Project metadata and dependencies
├── analysis_options.yaml    # Dart/Flutter lint configuration
└── README.md                # Project documentation

Application Flow

The intended application flow is:

Application Start
       │
       ▼
   Splash Screen
       │
       ▼
    Home Page
       │
       ├── About RU Fossil Park
       │
       ├── Invertebrates
       │
       ├── Vertebrates
       │
       └── Non-Fossils

main.dart

main.dart is the application entry point. It creates the initial
MaterialApp and displays an EasySplashScreen for five seconds before
navigating to AfterSplash.

The splash screen is configured with:

A yellow background.

A brown loader.

The text "Starting RU Fossil Park".

Placeholder text for the student's name, assignment title, and date.

A placeholder image path.

aftersplash.dart

AfterSplash creates the main MaterialApp and establishes named
routes for:

Invertebrates

Vertebrates

NonFossils

FossilPark

The home page is set as the application's initial screen after the
splash screen.

homepage.dart

The home page uses a yellow background and brown app bar and displays
the title RU Fossil Park.

It provides navigation buttons for the fossil park information and
fossil categories. The page also contains an image placeholder.

Dependencies

The pubspec.yaml file currently declares:

flutter

cupertino_icons

flutter_test

flutter_lints

However, main.dart imports:

package:easy_splash_screen/easy_splash_screen.dart

The easy_splash_screen package is not declared in the submitted
pubspec.yaml. This should be added before attempting to build the
application.

Current Issues / Required Work

The submitted project appears to be a partially completed
course/final-project template. The following issues were identified
during review.

1. Missing Dart screens

aftersplash.dart imports:

import 'fossilpark.dart';
import 'invertebrates.dart';
import 'vertebrates.dart';
import 'nonfossils.dart';

but these files are not present in the submitted lib/ directory.

As a result, the project cannot compile until these screens are created
or the imports/routes are removed.

2. Missing image assets

The application references placeholder image paths:

Image.asset("YOUR IMAGE")

and:

Image.asset('YourImage')

These are not valid asset files in the submitted project.

Actual image files should be added to the project and declared under the
flutter: section of pubspec.yaml, for example:

flutter:
  uses-material-design: true
  assets:
    - assets/images/

The Dart code should then reference the real asset paths.

3. Missing easy_splash_screen dependency

Because main.dart imports easy_splash_screen, the package needs to
be added to pubspec.yaml or the splash screen should be rewritten
using Flutter's built-in widgets.

4. Placeholder splash-screen information

The splash screen currently displays:

YOUR NAME

ASSIGNMENT TITLE

DATE

These should be replaced with the appropriate project/student
information.

5. Widget test does not match the application

test/widget_test.dart is still the default Flutter counter-app test.
It expects a counter displaying 0, an add button, and a value of 1.

The submitted application does not contain a counter, so this test does
not correspond to the actual RU Fossil Park application.

A better test suite should verify things such as:

The splash screen loads.

The home page contains "RU Fossil Park".

The navigation buttons exist.

Named routes open the appropriate pages.

6. Generated/build files are included

The submitted archive contains generated Flutter files and directories
such as .dart_tool/ and build/. These normally should not be
committed to a source repository because they can be regenerated by
Flutter.

The existing .gitignore should be retained, and generated files should
generally be excluded from future submissions.

Getting Started

After completing the missing source files and assets:

1. Install Flutter

Install the Flutter SDK and make sure it is available from your command
line.

Verify the installation with:

flutter doctor

2. Open the project

Change into the project directory:

cd final_dino1

3. Install dependencies

Run:

flutter pub get

If the easy_splash_screen package is retained, add the package to
pubspec.yaml before running this command.

4. Run static analysis

Use:

flutter analyze

Resolve any missing-file, dependency, asset, or lint errors reported by
the analyzer.

5. Run tests

Use:

flutter test

The default counter test should be replaced with tests appropriate to RU
Fossil Park.

6. Run the application

With a configured emulator, simulator, browser, or connected device:

flutter run

Suggested Development Priorities

To finish the project, the recommended implementation sequence is:

Add the missing fossil-category Dart screens.

Add and register the required image assets.

Add the easy_splash_screen dependency or replace it with a
built-in Flutter splash implementation.

Replace all placeholder text with final project information.

Improve the home-page layout and accessibility.

Replace the default counter widget test with application-specific
tests.

Run flutter analyze, flutter test, and flutter run.

Remove generated build artifacts from the source submission.

License

No license is specified in the submitted project. If this project will
be distributed publicly, add an appropriate license and document any
third-party images or other content used by the application.

Project Status

Status: Incomplete / Under Development

The archive contains the Flutter project foundation and the beginning of
the RU Fossil Park user interface, but the missing screens, assets, and
dependency configuration need to be addressed before the project is a
complete runnable application.
