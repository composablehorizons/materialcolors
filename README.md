# Material Colors

All Material Colors easily accessible from Jetpack Compose.

## Installation

```groovy
repositories {
    mavenCentral()
}
dependencies {
    implementation "com.composables.materialcolors:materialcolors:1.0.0"
}
```

## Example of usage

You can use it to setup your theme colors: 

```kotlin
@Composable
fun AppTheme(
    content: @Composable () -> Unit
) {
    MaterialTheme(
        colors = lightColorScheme(
            surfaceVariant = MaterialColors.Amber[100],
            primary = MaterialColors.Amber[800],
            onSurfaceVariant = MaterialColors.Brown[900],
            onSurface = MaterialColors.Amber[900]
        ),
        content = content
    )
}
```

Or you can use it to setup your colors in your composables:

```kotlin
Text("Hello world!", color = MaterialColors.Gray[900])
```

Android Studio (or IntelliJ IDEA) will display the preview of all colors, so you don't need to exit the IDE to check the colors:


## Looking for Jetpack Compose components?

Check out [Composables](https://www.composables.com/components) for a list of all official Jetpack Compose components and production ready components for your next big idea.

Made by Alex Styl ([@alexstyl](https://twitter.com/alexstyl)).