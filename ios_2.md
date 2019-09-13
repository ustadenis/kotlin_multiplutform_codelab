1. To rebuild uor comon module every time we need to add script to Build phase. 
To do it open **Build Phases** in target settings of your project.
2. Press + and choose **New Run Script Phase**
3. write the following script
```
cd "relativePathToCommonModule/build/xcode-frameworks"
./gradlew :common:packForXCode -PXCODE_CONFIGURATION=${CONFIGURATION}
```
4. Open **ViewController.swift**
5. Write the following code here
```swift
import CommonModule
***
override func viewDidAppear(_ animated: Bool) {
  ***
  title = CommonKt.printString()
}
```
