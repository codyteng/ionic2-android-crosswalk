# Ionic2 with Crosswalk Project

Assume:
1. you already have an working Ionic2 project with the name ionic2-project.
2. you have all dependencies added

Author: CodeDee

## Getting started

1. Change directory to YOUR ionic2 project
    ```
    cd ionic2-project
    ```
    
2. Add Crosswalk cordova plugin to your project
    ```
    ionic plugin add cordova-plugin-crosswalk-webview
    ```
    Now you should see **cordova-plugin-crosswalk-webview** appear under plugin folder
    |-- ionic2-project
        |-- app
        |-- node_modules
        |-- plugins
            |-- cordova-plugin-crosswalk-webview
            ...
        ...

3. Make sure that have installed latest version of **Android Support Repository** & **Google Repository**.
    ```
    android
    ```
    This will bring up Android SDK Manager, check if you have installed.
    
4. Add platform Android, if you have not
    ```
    ionic platform add android
    ```
    
5. Run project in Andrdoid device
    ```
    ionic run android
    ```
    
6. Now we have to verify if crosswalk is successfully packaged into your project.

    **Hint 1: Inspect the name of built APK**
    
        |-- ionic2-project
            |-- app
            |-- node_modules
            |-- plugins
            |-- platforms
                |-- android
                    |-- build
                        |-- outputs
                            |-- apk
                                |-- android-debug.apk **<-- if you see this, crosswalk isn't in**
                                ...
                            ...
                        ...
                    ...
                ...
            ...
        ...

    **Hint 2: Inspect useragent of your application with Google Chrome Developer Tools**
    
    Follow the following steps:
    1. Launch Google Chrome then launch **Developer Tools (⌥⌘I)**
    
    2. Attach your Android device to your machine
    
    3. Expand the 3-dots menu located at top right of the window, go to **More Tools > Inspect deivces...**
    
    4. You will now prompted with a Device windows
    
    5. Pick your Android device then under your ionic2 project click **Inspect**
    
    6. Key in below command in the console
        ```
        navigator.userAgent
        ```
    
    7. Verify your useragent string here:
        https://github.com/crosswalk-project/crosswalk-website/wiki/crosswalk-user-agent
        
    
Congratulation! You have successfully added Crosswalk into your Ionic2 project.
