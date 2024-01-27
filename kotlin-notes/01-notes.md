## Kotlin basics

### Hello World
```kotlin
fun main(){
    print("Hello World")
}
```

### The very basics
```kotlin
// creating a variable
val myVariable  = "Junaid"   // immutable
var myVariable2 = 1234       // mutable

// adding a datatype
// Common Types: Int, Float, Double, String, Boolean, Char
var myVar: Type = VALUE

// string interpolation
val interpolate = "Hello there $name, I'm ${myname.uppercase()}"

// Arithmetic operators: +, -, *, /, %, ++, --
// Comparison operators: ==, !=, <, >, <=, >=
```

### if-else
```kotlin
// if-else is just like any other language

if (myAge > yourAge) {
    println("I'm older than you")
} else if (myAge < yourAge) {
    println("You are older than me")
} else {
    println("We are the same age")
}
```

### when statement
```kotlin
// it replaces switch from java

when (season) {
    1 -> println("Spring")
    2 -> {
        println("Fall")
        println("Autumn")
    }
}

when(month){
    in 5..8 -> println("Spring")
    1, 2, 10, 11 -> println("Winter")
}
```

