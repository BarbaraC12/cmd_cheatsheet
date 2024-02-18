# Flutter Cheatsheet

## Widgets

### StatelessWidget

```dart
class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Text('Hello, Flutter!'),
    );
  }
}
```

### StatefulWidget

```dart
class MyStatefulWidget extends StatefulWidget {
  @override
  _MyStatefulWidgetState createState() => _MyStatefulWidgetState();
}

class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Text('Stateful Widget Example'),
    );
  }
}
```

## Layouts

### Column

```dart
Column(
  children: [
    Text('Item 1'),
    Text('Item 2'),
    Text('Item 3'),
  ],
)
```

### Row

```dart
Row(
  children: [
    Text('Item 1'),
    Text('Item 2'),
    Text('Item 3'),
  ],
)
```

### Stack

```dart
Stack(
  children: [
    Positioned(
      top: 10,
      left: 10,
      child: Text('Top Left'),
    ),
    Positioned(
      bottom: 10,
      right: 10,
      child: Text('Bottom Right'),
    ),
  ],
)
```

## State Management

### Provider

```dart
ChangeNotifierProvider(
  create: (context) => MyNotifier(),
  child: MyWidget(),
)
```

### Bloc

```dart
BlocProvider(
  create: (context) => MyBloc(),
  child: MyWidget(),
)
```

## Navigation

### Pushing to a new screen

```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondScreen()),
);
```

### Passing data to a new screen

```dart
Navigator.push(
  context,
  MaterialPageRoute(
    builder: (context) => SecondScreen(data: 'Hello from the first screen!'),
  ),
);
```

## HTTP Requests

### Using `http` package

```dart
import 'package:http/http.dart' as http;

final response = await http.get('https://api.example.com/data');
if (response.statusCode == 200) {
  print('Data: ${response.body}');
} else {
  print('Request failed with status: ${response.statusCode}');
}
```

## CMD Line

| CMD | Usage | About |
|-----|-------|-------|
| analyze | `flutter analyze -d <DEVICE_ID>` | Analyzes the project’s Dart source code. Use instead of `dart analyze`. |
| assemble | `flutter assemble -o <DIRECTORY>` | Assemble and build flutter resources.|
| attach | `flutter attach -d <DEVICE_ID>` | Attach to a running application.|
| bash-completion | `flutter bash-completion` | Output command line shell completion setup scripts.|
| build | `flutter build <DIRECTORY>` | Flutter build commands.|
| channel | `flutter channel <CHANNEL_NAME>` | List or switch flutter channels.|
| clean | `flutter clean` | Delete the build/ and .dart_tool/ directories.|
| config | `flutter config --build-dir=<DIRECTORY>` | Configure Flutter settings. To remove a setting, configure it to an empty string.|
| create | `flutter create <DIRECTORY>` | Creates a new project.|
| custom-devices | `flutter custom-devices list` | Add, delete, list, and reset custom devices.|
| devices | `flutter devices -d <DEVICE_ID>` | List all connected devices.|
| doctor | `flutter doctor` | Show information about the installed tooling.|
| downgrade | `flutter downgrade` | Downgrade Flutter to the last active version for the current channel.|
| drive | `flutter drive` | Runs Flutter Driver tests for the current project.|
| emulators | `flutter emulators` | List, launch, and create emulators.|
| gen-l10n | `flutter gen-l10n <DIRECTORY>` | Generate localizations for the Flutter project.|
| help | `flutter help <command>` | Use for additional help. |
| install | `flutter install -d <DEVICE_ID>` | Install a Flutter app on an attached device.|
| logs | `flutter logs` | Show log output for running Flutter apps.|
| precache | `flutter precache <ARGUMENTS>` | Populates the Flutter tool’s cache of binary artifacts.|
| pub | `flutter pub <PUB_COMMAND>` | Works with packages. Use instead of `dart pub`.|
| run | `flutter run <DART_FILE>` | Runs a Flutter program.|
| screenshot | `flutter screenshot` | Take a screenshot of a Flutter app from a connected device.|
| symbolize | `flutter symbolize --input=<STACK_TRACK_FILE>` | Symbolize a stack trace from the AOT compiled Flutter application.|
| test | `flutter test <DIRECTORY>` | Runs tests in this package. Use instead of `dart test`.|
| upgrade | `flutter upgrade` | Upgrade your copy of Flutter.|

### Create a new project with specific options

- Custom package name:  
 ex: From com.dsn.package_app `flutter create --org=com.dsn package_app `
- Different app name and folder name:  
  ex: `flutter create --project-name=project_name folders_app`
- Platform-specific native language:  
  ex1: The native platform Android languages Java and Kotlin (default). `flutter create --android-language=java flutter_app`  
  ex2: The native platform for iOS languages Objective C and Swift (default). `flutter create --ios-language=objc flutter_app`
- Change native language :  
  ex: You may have to recode your logic according to new platform-specific language. `flutter create --android-language=java --ios-language=objc flutter_app`
