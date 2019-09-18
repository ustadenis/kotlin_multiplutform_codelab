1. To rebuild your comon module every time we need to add script to Build phase. 
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
6. Run application

[Prev](https://github.com/ustadenis/kotlin_multiplutform_codelab/blob/master/1_0_IOS.md)
[Next](https://github.com/ustadenis/kotlin_multiplutform_codelab/blob/master/2_0.md)
