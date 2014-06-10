android-studio-unit-test-plugin
===============================

Android Studio IDE support for Android gradle unit tests. Prepared for Robolectric.

This plugin will mark test directories and resolve `testCompile` dependencies. It also sets up the correct system properties for Robolectric.

![alt tag](https://raw.githubusercontent.com/evant/android-studio-unit-test-plugin/master/screenshots/idea.png)

## Install IDE the plugin
In Android Studo go to `Settings -> Plugins -> Browse Repositories...` and search for 'Android Studio Unit Test'.

If you feel like living on the edge, can download the [zip](https://github.com/evant/android-studio-unit-test-plugin/raw/master/AndroidStudioUnitTestPlugin/AndroidStudioUnitTestPlugin.zip) then go to `Settings -> Plugins -> Install plugin from disk..` to install.

## Install the gradle plugin
Currently you need the latest version of JCAndKSolutions's android-unit-test gradle plugin. It's not yet on maven central. Therefore, your steps are:

1. Install the forked version of android-unit-test.

  ```bash
  git clone https://github.com/JCAndKSolutions/android-unit-test.git
  cd android-unit-test
  gradle install
  ```

2. Set up the plugin as described [here](https://github.com/JCAndKSolutions/android-unit-test).

  The only difference is you need to point to the forked version you installed before.
  ```groovy
  buildscript {
    dependencies {
      repositories {
        mavenCentral()
        mavenLocal()
      }

      classpath 'com.github.jcandksolutions.gradle:android-unit-test:1.2.2-SNAPSHOT'
    }
  }
  ```
