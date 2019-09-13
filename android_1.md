1. Clone repository https://github.com/ustadenis/MultiplatformAndroid.git in the same directory as your kotlin multiplatform project.
2. Add the following code to **settings.gradle**
```groovy
include ':app'
include ':common'
rootProject.name='MultiplatformApp'

project(':common').projectDir = new File(settingsDir, 'relative path to common module')
enableFeaturePreview('GRADLE_METADATA')
```
