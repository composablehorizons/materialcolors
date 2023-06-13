# Material Colors

A little utility that brings all Material Colors from the 2014 pallet to your Jetpack Compose project.

## Why does this exist

I was tired of copy-pasting new colors every time I needed a new color for my new projects.

So instead of copy-pasting, it is now a dependency instead.

## Installation

```groovy
repositories {
    mavenCentral()
}
dependencies {
    implementation "com.composables:materialcolors:1.0.0"
}
```

## A richer selection of colors

The `Colors` class that comes with Jetpack Compose provides a few default colors but they are limited and not very exciting.

`MaterialColors` provides a richer set of colors that you can use in your project:

```kotlin
Text("Hello world!", color = MaterialColors.Gray[900])
```

## Should I use this to create my color scheme? 

In modern versions of Android, the system can generate the colors for you, [using Material You](https://www.composables.com/tutorials/theming). 

Those colors are picked automatically from the user's set wallpaper and it is the recommended way to create your color scheme.

If you still want to create a color scheme with fixed colors you can do it like this:

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

## Looking for Jetpack Compose components?

Check out [Composables](https://www.composables.com/components) for a list of all official Jetpack Compose components and production ready components for your next big idea.

Made by Alex Styl ([@alexstyl](https://twitter.com/alexstyl)).