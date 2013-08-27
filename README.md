Gradle-Build-Example
====================

This project does not contain any real code other than Gradle build-related files. It provides an example of how to build unique build variants that can be installed alongside eachother when the codebase has components that do not conform to the new build system. An example is an app that defines a ContentProvider, which must have a unique authority on the device. Another example is the Google Maps v2 API key which is generated on a packageName/signing key basis and Gradle Android does not have a simple solution to selecting the right key in an automated fashion.

Look at the build.gradle file. Notice how you can run install all combinations of the productFlavor x buildVariant alongside eachother. Example usage: "./gradlew installFreeAlpha", "./gradlew installPaidBeta", etc...
