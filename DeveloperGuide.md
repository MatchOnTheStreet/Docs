# Developer Guide

##Table of Contents
1. Obtaining the Source Code
2. Directory Structure
3. Opening the Project in an IDE
4. Building the Project
5. Testing Location Services
6. Unit Tests
7. Nightly Builds
8. Releasing a New Version
9. Bug reports
10. Design Patterns

##Obtaining the Source Code
To get the source code for Match on the Street, visit [this link to our github page](http://matchonthestreet.github.io/MatchOnTheStreet/). For direct access to our repository, visit [this link](https://github.com/MatchOnTheStreet/MatchOnTheStreet). 

For more information on how to use Github, visit [this link](https://help.github.com/).

##Directory Structure
The directory structure follows the standard layout for Android apps being developed in Android Studio.

The following describes the primary directories and their contexts.

1. `MatchOnTheStreet/tree/master/app/src/main/res/layout/`
	* Contains the layout files. These files describe the UI elements using xml.
2. `MatchOnTheStreet/tree/master/app/src/main/res/values/`
	* Contains the values used in the application. For example, one of the
	layouts may reference “@string/event_location_hint”, which is actually
	located in the file strings.xml in this directory. This is a handy place to keep all the values
	that may later change.
3. `MatchOnTheStreet/tree/master/app/src/main/java/com/cse403/matchonthestreet/`
	* Contains all of the java files that handle the logic of the application. This folder is
	where most of the code will be written. You can see the application logic bound to
	each view by looking at the objects whose name ends with Activity. For example
	the UI element defined by the layout activity_add_event.xml is handled by the java
	object AddEventActivity.java.
4. `MatchOnTheStreet/blob/master/app/src/main/AndroidManifest.xml`
	* The manifest file presents essential information about the app to the Android system.
	You will need to modify this file when you add new UI elements or change in some way
	how the application interacts with the android environment.

Note that the directories may appear differently when viewed in android studio.

##Opening the Project in an IDE
The application is mainly developed using [Android Studio](https://developer.android.com/tools/studio/index.html) based on [IntelliJ IDEA](https://www.jetbrains.com/idea/). Another valid option for the IDE would be [Eclipse](https://eclipse.org/). Here is a [tutorial](http://www.instructables.com/id/How-To-Setup-Eclipse-for-Android-App-Development/) on how to set up the Android Software Development Kit in Eclipse. The following instructions will be based on Android Studio.

To import this project from Github, you need to install [Git](https://git-scm.com/). One simple way of doing this is through installing [GitHub Desktop](https://desktop.github.com/).

Once you have Git installed, open Android Studio. If you see the window "Welcome to Android Studio", click on "Check out project from Version Control".

![as-welcome](https://github.com/MatchOnTheStreet/Docs/blob/master/img/5-opening-checkout.png)

Otherwise, in the menu bar, choose "File"->"New"->"Project from Version Control"->"GitHub"

![as-import-cvs](https://github.com/MatchOnTheStreet/Docs/blob/master/img/5-opening-dropdownlist.png)

In the popup window, type in the URL (https://github.com/MatchOnTheStreet/MatchOnTheStreet) of the repository to be checked out, along with other required information. Follow the instructions given by Android Studio, and the project import should be successful. Note that it might take up to several minutes for Android Studio to sync and build the project.

![as-import-window](https://github.com/MatchOnTheStreet/Docs/blob/master/img/5-opening-window.png)

[Here](http://javapapers.com/android/android-studio-git-tutorial/) is a useful tutorial on using CVS on Android Studio.

##Building the Project
The application is built using the integrated build system [Gradle](http://developer.android.com/sdk/installing/studio-build.html) of Android Studio. 
Normally, Gradle will automatically build the project after it is opened in Android Studio. To manually do this, click on the “Build” option in the menu bar, and then choose “Rebuild project”.

![menubar](https://github.com/MatchOnTheStreet/Docs/blob/master/img/1-menubar.png)

Other options, such as making the project and generating the APK package, could also be accessed under this menu.

You can also use the command line. On the root of the project you can run

	./gradlew assembleDebug

Which will build the project in debug mode. You can also run

	./gradlew clean

To remove any files created from the build. 
See [this link](http://developer.android.com/tools/building/building-cmdline.html) for more information on building on the command line.

The build process of Gradle follows the procedures denoted by the following diagram: 

![process-img](https://github.com/MatchOnTheStreet/Docs/blob/master/img/2-diagram.png)

##Testing Location Services
Since this app requires your location, you will need to give it permissions in the settings of your device:
Open the settings app within the emulator
Under the 'Device' subheading click the 'Apps'
Find 'Match on the Street'
Click 'Permissions'
Turn location services on
This should get changed later to be turned on through a popup dialogue like most other apps.

Note that the emulator will not emulate location services automatically, you must open a terminal and send it coordinates:
‘telnet localhost 5554’
The format is: ‘geo fix <longitude> <latitude>’ 
so doing 'geo fix -122.31544733 47.6528135881'  will show your location on UW campus

![cmdline](https://github.com/MatchOnTheStreet/Docs/blob/master/img/3-cmdline.png)

##Unit Tests
Unit tests can be found under `.../MatchOnTheStreet/app/src/test/java/com/cse403/matchonthestreet/`. You should be able to run it directly from Android Studio: 

The Android Plugin for Gradle compiles the local unit test code located in the default directory (src/test/java), builds a test app, and executes it locally using the default test runner class.

To run local unit tests in your Gradle project from Android Studio:

1. In the Project window, right click on the project and synchronize your project.
2. Open the Build Variants window by clicking the left-hand tab, then change the test artifact to Unit Tests.
3. In the Project window, drill down to your unit test class or method, then right-click and run it. To run all tests in the unit test directory, select the directory then right-click and press Run tests.
4. Android Studio displays the results of the unit test execution in the Run window.

To run local unit tests in your Gradle project from the command-line, call the test task command.

`./gradlew test`

If there are failing tests, the command will display links to HTML reports (one per build variant). You can find the generated HTML test result reports in the <path_to_your_project>/app/build/reports/tests/ directory, and the corresponding XML files in the <path_to_your_project>/app/build/test-results/ directory.

For more information on creating and conducting unit tests in Android Studio, follow [this link](http://developer.android.com/training/testing/start/index.html#run-local-tests).

##Nightly Builds
Follow [this guide](http://www.developerfiles.com/how-to-send-emails-from-localhost-mac-os-x-el-capitan/) to configure sendmail on mac:

Add a cronjob though the terminal:
	
	crontab -e

This should open the editor, so add:
	
	MAILTO=”your_email”
	*/10 23 * * * <path to ci.sh> <base_directory> <name_of_tmp_directory> <path_to_android_sdk>

Note that the file should have an empty line at the end.


##Releasing a New Version
After an updated version of the project is built and tested, it is recommended to use Gradle to generate the compiled APK file. Then the project should be pushed from local repository to the `master` branch on our repository(https://github.com/MatchOnTheStreet/MatchOnTheStreet). 

After the files in the master branch are updated, the related download links should also be added on the `README.md` file  and the [Product Website](http://matchonthestreet.github.io/MatchOnTheStreet/).

###Download links for .apk, .tar.gz, .zip files:
* _.apk file:_ Normally, the `.apk` file would be stored under `https://github.com/MatchOnTheStreet/MatchOnTheStreet/app/build/outputs/apk`. 
* _.tar.gz file:_ `https://github.com/MatchOnTheStreet/MatchOnTheStreet/tarball/master`
* _.zip file:_ `https://github.com/MatchOnTheStreet/MatchOnTheStreet/zipball/master`

###Updating the website:
The [Product Website](http://matchonthestreet.github.io/MatchOnTheStreet/) is generated using the [Github Pages](https://pages.github.com/), and is store under the `gh-pages` branch of the project repository.  To add the download links to the website, open `index.html` and look for `<aside>` tags like the following, then modify the `href` attribute of the corresponding download links.

![html-img](https://github.com/MatchOnTheStreet/Docs/blob/master/img/4-html.png)

##Bug reports
Currently we are using [a public Google Form](http://goo.gl/forms/Y5O8jgcr0i) to register bug reports. A complete record of existing bugs could be accessed [here](https://docs.google.com/spreadsheets/d/164tTaI434cTdc8Asoq-i0H_Auo0y6LtOJhLn8qNfMXQ/edit).

##Design Patterns
* Singleton pattern
	* The `DBManager` Class uses the Singleton Pattern. It does not make sense
	for the application to have more than one DBManager. For that reason the
	the class has been made static, and given a private constructor.
* Factory pattern
	* In the `ListViewActivity`, we implemented  `SetTextDatePickerDialog` using the Factory Pattern. Because the `DatePickerDialog` objects for different entry fields are just trivially different, we used a getPick() method inside this class instead of calling different constructors everytime. By doing so the code redundancy was reduced effectively.
