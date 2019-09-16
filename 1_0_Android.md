1. Clone repository https://github.com/ustadenis/MultiplatformAndroid.git in the same directory as your kotlin multiplatform project.
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
