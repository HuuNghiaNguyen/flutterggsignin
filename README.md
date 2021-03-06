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

* Type **Project name** and click **Continue**
<p align="center"><img src="./asset/step1.PNG" width="400" alt="Step 1" title=""></p>

* (Optional) Enable **Enable Google Analytics for this project** and click **Continue**
<p align="center"><img src="./asset/step2.PNG" width="400" alt="Step 2" title=""></p>

* Choose account and click **Create project**
<p align="center"><img src="./asset/step3.PNG" width="400" alt="Step 3" title=""></p>

* Choose desired platform to continue
<p align="center"><img src="./asset/step4.PNG" width="400" alt="Step 4" title=""></p>

### 2. Customize config:
#### Register app:<br>
* **Andoird package name** : Your android app name
* **Debug signing certificate SHA-1**: Your app hash code, you can obtain one by run command:

> $ keytool -list -v \-alias androiddebugkey -keystore %USERPROFILE%\.android\debug.keystore

<p align="center"><img src="./asset/step5.PNG" width="400" alt="Step 5" title=""></p>

#### Download config file
Download and save **google-services.json** file to **android** folder

#### Add firebase SDK to project:
Copy those code to **build.gradle** (in project folder):<br>

> buildscript {<br>
> &nbsp;&nbsp;&nbsp;&nbsp; repositories {<br>
> &nbsp;&nbsp;&nbsp;&nbsp;    // Check that you have the following line (if not, add it):<br>
> &nbsp;&nbsp;&nbsp;&nbsp;    google()  // Google's Maven repository<br>
>  }<br>
>  dependencies {<br>
>  &nbsp;&nbsp;&nbsp;&nbsp;   ...<br>
>  &nbsp;&nbsp;&nbsp;&nbsp;   // Add this line<br>
>  &nbsp;&nbsp;&nbsp;&nbsp;   classpath 'com.google.gms:google-services:4.3.5'<br>
>  }<br>
> }<br>
> <br>
> &nbsp;&nbsp;&nbsp;&nbsp; allprojects {<br>
> &nbsp;&nbsp;&nbsp;&nbsp;  ...<br>
> &nbsp;&nbsp;&nbsp;&nbsp;  repositories {<br>
> &nbsp;&nbsp;&nbsp;&nbsp;    // Check that you have the following line (if not, add it):<br>
> &nbsp;&nbsp;&nbsp;&nbsp;    google()  // Google's Maven repository<br>
> &nbsp;&nbsp;&nbsp;&nbsp;    ...<br>
> &nbsp;&nbsp;&nbsp;&nbsp;  }<br>
> }<br>

#### Resync project by run this code:
> cd android .\gradlew --refresh-dependencies

## ![Build project and enjoy!](https://via.placeholder.com/15/00ff005/000000?text=+) `Build project and enjoy!`
