1. Navigate to your common module folder and run command **./gradlew :common:packForXcode**
2. Open target settings of your ios project
3. Click + of **Embedded Binaries** section
4. Click **Add Other...**
5. Choose ios framework of your common module **common/build/xcode-frameworks/CommonModule.framework**
6. Uncheck **Copy items if needed** and choose **Create folder reference** option. Then press finish
7. Open **Build Settings** of your project
8. Find **Framework Search Paths** and put relative path to **build/xcode-frameworks** of your project
9. Try to build the application
