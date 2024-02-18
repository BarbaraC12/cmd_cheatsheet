# Flutter cmd cheat sheet

| CMD | usage | about |
|--|--|--|
| analyze	| `flutter analyze -d <DEVICE_ID>` |	Analyzes the project’s Dart source code. Use instead of `dart analyze`. |
| assemble |	`flutter assemble -o <DIRECTORY>`|	Assemble and build flutter resources.|
| attach |	`flutter attach -d <DEVICE_ID>`|	Attach to a running application.|
| bash-completion	|`flutter bash-completion`	| Output command line shell completion setup scripts.|
| build |	`flutter build <DIRECTORY>`|	Flutter build commands.|
| channel |	`flutter channel <CHANNEL_NAME>`|	List or switch flutter channels.|
| clean	| `flutter clean`	| Delete the build/ and .dart_tool/ directories.|
| config	| `flutter config --build-dir=<DIRECTORY>`|	Configure Flutter settings. To remove a setting, configure it to an empty string.|
| create	| `flutter create <DIRECTORY>`|	Creates a new project.|
| custom-devices	| `flutter custom-devices list`| 	Add, delete, list, and reset custom devices.|
| devices	| `flutter devices -d <DEVICE_ID>`|	List all connected devices.|
| doctor	| `flutter doctor`	| Show information about the installed tooling.|
| downgrade	| `flutter downgrade`	| Downgrade Flutter to the last active version for the current channel.|
| drive	| `flutter drive`	| Runs Flutter Driver tests for the current project.|
| emulators	| `flutter emulators`	| List, launch and create emulators.|
| gen-l10n	| `flutter gen-l10n <DIRECTORY>`|	Generate localizations for the Flutter project.|
| help | `flutter help <command> `| Use for additional help. |
| install	| `flutter install -d <DEVICE_ID>`|	Install a Flutter app on an attached device.|
| logs	| `flutter logs	| Show log output for running Flutter apps.|
| precache	| `flutter precache <ARGUMENTS>`|	Populates the Flutter tool’s cache of binary artifacts.|
| pub	| `flutter pub <PUB_COMMAND>`|	Works with packages. Use instead of `dart pub`.|
| run	| `flutter run <DART_FILE>`|	Runs a Flutter program.|
| screenshot	| `flutter screenshot`	| Take a screenshot of a Flutter app from a connected device.|
| symbolize	| `flutter symbolize --input=<STACK_TRACK_FILE>`|	Symbolize a stack trace from the AOT compiled flutter application.|
| test	| `flutter test <DIRECTORY>`	| Runs tests in this package. Use instead of `dart test`.|
| upgrade	| `flutter upgrade`	| Upgrade your copy of Flutter.|


## 1. Create a new project with specific options

- Custom package name:  
 ex: From com.dsn.package_app `flutter create --org=com.dsn  package_app `
- Different app name and folder name:  
  ex: `flutter create --project-name=project_name folders_app`
- Platform-specific native language:  
  ex1: The native platform Android languages Java and Kotlin (default). `flutter create --android-language=java flutter_app`  
  ex2: The native platform for iOS languages Objective C and Swift (default). `flutter create --ios-language=objc flutter_app`
- Change native language :  
  ex: You may have to recode your logic according to new platform-specific language. `flutter create --android-language=java --ios-language=objc flutter_app`
