1. Open AndroidApp project in AndroidStudio.
2. Add the following code to **settings.gradle**
```groovy
include ':app'
include ':common'
rootProject.name='MultiplatformApp'

project(':common').projectDir = new File(settingsDir, 'relative path to common module')
enableFeaturePreview('GRADLE_METADATA')
```
3. Add implemetation in app **build.gradle**
```groovy
dependencies {
    ***
    implementation project(":common")
}
```
4. Sync gradle

[Prev](https://github.com/ustadenis/kotlin_multiplutform_codelab/blob/master/0_4.md)
[Next](https://github.com/ustadenis/kotlin_multiplutform_codelab/blob/master/1_1_Android.md)
