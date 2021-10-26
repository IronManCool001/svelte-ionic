This is the svelteionic template bootstraped by sapper.

Make sure to change the appID in the capacitor.config.json

# Installing the dependencies
Enter the following command to install the dependencies:
npm i or yarn i (Based on your package manager)


# Starting the server
enter the following commandd into your cmd/cli:
[<br>]
npm dev

# Building the app
Enter the follwoing command to build your app:
[<br>]
ionic build

# Running the app in android studio
Type the following code in your cmd/cli to run the app in Android Studio:
[<br>]
Make sure to set the set Android Gradle Plugin Version as 3.6.1 and Gradle version as 6.2.1 in the Project Structure from the file menu of Android Studio oor your app may not compile.
[<br>]
ionic build
[<br>]
ionic cap open android