1. Navigate to your common module folder and run command **./gradlew :common:packForXcode**
2. Clone project **https://github.com/ustadenis/MultiplatformIOS** in the same directory as your kotlin multiplatform project
3. Open target settings of your ios project
4. Click + of **Embedded Binaries** section
5. Click **Add Other...**
6. Choose ios framework of your common module **common/build/xcode-frameworks/CommonModule.framework**
7. Uncheck **Copy items if needed** and choose **Create folder reference** option. Then press finish
8. Open **Build Settings** of your project
9. Find **Framework Search Paths** and put relative path to **build/xcode-frameworks** of your project
10. Try to build the application
