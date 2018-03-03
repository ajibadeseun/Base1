# Base1
This is app that shows how to apply material design guidelines in android application development

# Screnshots

<img src="https://github.com/ajibadeseun/Base1/blob/master/Screenshot_20180303-173851.png" width="300" height="450" />
<img src="https://github.com/ajibadeseun/Base1/blob/master/Screenshot_20180303-173900.png" width="300" height="450" />
<img src="https://github.com/ajibadeseun/Base1/blob/master/Screenshot_20180303-173905.png" width="300" height="450" />
<img src="https://github.com/ajibadeseun/Base1/blob/master/Screenshot_20180303-173911.png" width="300" height="450" />
<img src="https://github.com/ajibadeseun/Base1/blob/master/Screenshot_20180303-173916.png" width="300" height="450" />
<img src="https://github.com/ajibadeseun/Base1/blob/master/Screenshot_20180303-173928.png" width="300" height="450" />

# Gradle
Make sure your build.gradle(Module:app) file looks as follows:

    apply plugin: 'com.android.application'

    android {

    compileSdkVersion 26
    buildToolsVersion '26.0.2'
    defaultConfig {
        applicationId "com.treble.base1"
        minSdkVersion 17
        targetSdkVersion 26
        versionCode 1
        versionName "1.0"
        testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"
        vectorDrawables.useSupportLibrary = true
    }
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
    }

    dependencies {

    compile fileTree(dir: 'libs', include: ['*.jar'])
    androidTestCompile('com.android.support.test.espresso:espresso-core:2.2.2', {
        exclude group: 'com.android.support', module: 'support-annotations'
    })
    compile 'com.android.support:appcompat-v7:26.+'
    compile 'com.android.support:design:26.1.0'
    compile 'com.android.support:recyclerview-v7:26.1.0'
    compile 'com.android.support:cardview-v7:26.1.0'
    compile 'com.android.support.constraint:constraint-layout:1.0.2'
    testCompile 'junit:junit:4.12'
    }
 
And your build.gradle(Project:app) looks like the following:

    // Top-level build file where you can add configuration options common to all sub-projects/modules.

     buildscript {
    repositories {
        jcenter()
        google()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.0.1'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
     }
    }

    allprojects {
    repositories {
        jcenter()
        maven {
            url "https://maven.google.com"
        }
        google()
     }
    }

    task clean(type: Delete) {
    delete rootProject.buildDir
    }
  

