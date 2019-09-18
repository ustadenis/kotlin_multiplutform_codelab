1. Navigate to your common module folder and run command **./gradlew :common:packForXcode** (if you don't have environment variable JAVA_HOME use command **export JAVA_HOME=/Applications/Android\ Studio.app/Contents/jre/jdk/Contents/Home/**)
2. Open ios project **IOSApp** with XCode.
3. Open target settings of your ios project.
4. Click + of **Embedded Binaries** section.
5. Click **Add Other...**.
6. Choose ios framework of your common module **common/build/xcode-frameworks/CommonModule.framework**.
7. Uncheck **Copy items if needed** and choose **Create folder reference** option. Then press finish.
8. Open **Build Settings** of your project.
9. Find **Framework Search Paths** and put relative path to **build/xcode-frameworks** of your project.
10. Try to build the application.

[Next](https://github.com/ustadenis/kotlin_multiplutform_codelab/blob/master/1_1_IOS.md)
