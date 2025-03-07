Add the following dependencies from the below link at the **app** level gradle file
https://developer.android.com/jetpack/androidx/releases/navigation

val nav_version = "2.8.8"

// Jetpack Compose integration
implementation("androidx.navigation:navigation-compose:$nav_version")

// Views/Fragments integration
implementation("androidx.navigation:navigation-fragment:$nav_version")
implementation("androidx.navigation:navigation-ui:$nav_version")

// Feature module support for Fragments
implementation("androidx.navigation:navigation-dynamic-features-fragment:$nav_version")

under **plugin** {
  id("androidx.navigation.safeargs.kotlin")
}

Add the following dependencies in the **project** level gradle file
buildscript {
    repositories {
        google()
    }
    dependencies {
        classpath(libs.androidx.navigation.safe.args.gradle.plugin)
    }
}

To add the navigation component, right click on the app -> New -> Android Resource File -> give the **File Name**  as **nav_graph**, select **Resource Type** as **Navigation**
Now, the navigation folder gets created under the res folder with nav_graph.xml file in it
