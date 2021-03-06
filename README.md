# Deckard

Deckard is the simplest possible Android project that uses Robolectric for testing and Maven to build. It has one Activity (with an empty layout), and a Robolectric test that creates that Activity. 

Deckard also imports seamlessly into IntelliJ, due to IntelliJ's support for Maven. Just import the pom.xml.

## Setup

To start a new Android project:

1. Install the [Android SDK](http://developer.android.com/sdk/index.html). On Mac OS X with [Homebrew](http://brew.sh/) just run:
    ```bash
    brew install android-sdk
    ```

2. Set your `ANDROID_HOME` environment variable to `/usr/local/Cellar/android-sdk/<version>`.

3. Run the Android SDK GUI and install API 18 and any other APIs you might need. You can start the GUI like so:
    ```bash
    android
    ```

4. Use [Maven Android SDK Deployer](https://github.com/mosabua/maven-android-sdk-deployer) to maven-ize the Android SDK:
    ```bash
    git clone https://github.com/mosabua/maven-android-sdk-deployer.git
    (cd maven-android-sdk-deployer && mvn install -P 4.3)
    ```

5. Download Deckard from GitHub:
    ```bash
    wget https://github.com/robolectric/deckard/archive/master.zip
    unzip master.zip
    mv deckard-master my-new-project
    ```

6. In the project directory you should be able to run the tests:
    ```bash
    cd my-new-project
    mvn clean test
    ```
        
7. Optionally, import the project into IntelliJ (or Eclipse) by selecting 'Import Project' in IntelliJ and selecting the project's `pom.xml`. When prompted to pick an SDK you just need to select the Android SDK home and your JDK.

8. Change the names of things from 'Deckard' to whatever is appropriate for your project. Package name, classes, and the AndroidManifest are good places to start.

9. Build an app. Win.
