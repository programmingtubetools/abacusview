
# AbacusView

Easy abacus control to add in Android Studio Projects.
The AbacusView provides you prebuilt basic Abacus in your projects
wherever you need.




## Installation

To start using AbacusView in your project, just add it to dependecy
and add `com.coearners.abacus:AbacusView:1.0.0-beta01`

```gradle
  dependencies{
  ..
    implementation 'com.coearners.abacus:AbacusView:1.0.0-beta01'
  ..
  }
```
    
## Documentation

[Documentation and API Reference]()




## Usage/Examples

### Adding AbacusView to your layout.
Setting `layout_width` and `layout_height` to `wrap_content` automatically handles 
the width of the width and height of AbacusView according to screen size.   
The changes made in `layout_height` property doesn't change the scale of the controls.
The default and fixed height for AbacusView is `200sp`.
```xml
<com.coearners.abacus.AbacusView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"/>
```

### Getting the value of AbacusView
```java
AbacusView abacusView = findViewById(R.id.abacusView);
// Get the value of abacus.
...
/*
getValue() returns the value of the abacus to maximum  
3 digits of precision.
*/
double value = abacusView.getValue();
...
```
### Getting truncated string value of AbacusView
```java
// Getting string value.
...
/*
getStringValue() returns the value in string data type.   
It also takes care of integral values sent by   
getValue() value function and reduces the precision   
i.e. it truncates the decimal points if not required.
e.g. 
    For value = 1.212
        getValue() returns 1.212 as double  
        getStringValue() returns 1.212 as string
    For value = 1.000
        getValue() returns 1.0 as double
        getStringValue() retunrs 1 as string
*/
String value = abacusView.getStringValue();
...
```
### Resetting the AbacusView
```java
// Resetting the abacus
...
/*
reset() function can be used to reset the beads of the abacus  
to their default positions
*/
abacusView.reset();
...
```