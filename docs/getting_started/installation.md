# <span class="emoji"> :material-download: </span> Installation

This guide explains how to install the Indoor Navigation Engine library in your Android project.

## <span class="emoji"> :material-wrench-cog: </span> Prerequisites

Before you begin, ensure you have the following prerequisites installed:

- Android Studio
- JDK 17
- Android SDK with minimum SDK version 24 and target SDK version 34
- Gradle 8.2

## <span class="emoji"> :octicons-diff-added-16: </span> Dependency Installation

To integrate the Indoor Navigation Engine library into your Android project, follow these steps:

### <span class="emoji"> :simple-gradle: </span> Gradle

1. Open your project's `build.gradle` file.
2. Add the following dependency in the `dependencies` block:

=== "Groovy DSL"
      ```groovy
          dependencies {
            implementation 'com.machinestalk:indoornavigationengine:1.0.0'
          }
      ```
=== "Kotlin DSL"
      ```kotlin
          dependencies {
            implementation("com.machinestalk:indoornavigationengine:1.0.0")
          }
      ```




### <span class="emoji"> :simple-apachemaven: </span> Maven

1. Open your project's `pom.xml` file.
2. Add the following dependency:

    ```xml
    <dependency>
        <groupId>com.machinestalk</groupId>
        <artifactId>indoornavigationengine</artifactId>
        <version>1.0.0</version>
        <type>pom</type>
    </dependency>
    ```

!!! warning end "Java 17 Required"

    this library uses [Filament]() a native library written in C++ for rendering 3D graphics, its api is exposed to Java using JNI,
    and the JNI api is compiled with Java 17, so you need to compile your project with Java 17. 
    Ensure your `build.gradle` file is configured accordingly:

    ```groovy
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_17
        targetCompatibility JavaVersion.VERSION_17
    } 
    kotlinOptions {
        jvmTarget = '17'
    }
    ```
