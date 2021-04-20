# SIMPLE GOOGLE LOG IN - FLUTTER APP
<p float="left" align="center">
<img src="./asset/flutter.png" width="100" alt="Flutter icon" title="Flutter">
<img src="./asset/add.png" width="100" alt="Flutter icon" title=" and ">
<img src="./asset/gg.png" width="100" alt="Flutter icon" title=" Google ">
 </p>
 <br><br><br>

## ![Preparation](https://via.placeholder.com/15/00ff005/000000?text=+) `Preparation`
### 1. Install Flutter:
You must have a working Flutter installed, if not, follow instruction here to get it ready: [Flutter installation guide](https://flutter.dev/docs/get-started/install)

### 2. Create a new flutter project in **VS Code**:
* Open the Command Palette (*Ctrl+Shift+P* on Windows or *Cmd+Shift+P* on MacOS)
* Select **Flutter: New Application Project** command and press **Enter**
* Enter the **Project name**
* Select a **Project location**

### 3. Get the required package (**google_sign_in**):
* Run this command:
> $ flutter pub pub add google_sign_in

* (Or) Manually add this line to pubspec.yaml:
> dependencies:<br>
> &nbsp;&nbsp;google_sign_in: ^5.0.2

and run this command:

> $ flutter pub get

### 4. Import package into project:
Copy this line to the header of file:

> import 'package:google_sign_in/google_sign_in.dart';


## ![Create app](https://via.placeholder.com/15/00ff005/000000?text=+) `Create app`
Replace the default main file (Counter App) with those code lines: [Sign_in code](https://pub.dev/packages/google_sign_in/example) 
```diff
- NOTE: This app will not properly run at this point!
```


## ![App integration](https://via.placeholder.com/15/00ff005/000000?text=+) `App integration`
### 1. Add a project to Firebase:

* Open Firebase page: [Firebase link](https://firebase.google.com/?platform=android)

* Click **Get started**
<p align="center"><img src="./asset/started.PNG" width="400" alt="Get started" title=""></p>

* Click **Add project**
<p align="center"><img src="./asset/addproject.PNG" width="400" alt="Add project" title=""></p>
