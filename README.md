# Guide
Swift: A Quick Reference Guide
## Literals ##
A literal is simply a numeric or string value. 
Числовой литерал — это фиксированная последовательность цифр, на- чинающаяся либо с цифры, либо с префиксного оператора «минус» или «плюс» . Так, например, «2», «–64», «+18» — все это числовые литералы . 

1. Numeric Literals
2. Integer Literals(1234 )
3. Floating Point Literals (12.34)
4. String Literals ("Archer")
## Basic Types ##
Every constant or variable in your program has a type. Basic types: Int, Double, String, Bool. 
1. Int and Double Types (let HD = 24, let PP = 2.2)
2. Characters and Strings ("spark", "!")
3. Bool ("true" and "false")
### Declarations and Assignments ###
One uses "let" to create a constant and the other uses "var" to create a variable. Constants created with let must have an initial value and cannot be modified.
Объявление — это создание нового объекта (хранилища данных) . Инициализация — это присвоение объявленному объекту определен-
ного значения . ( AssignmentsyearSince1970 = secondsSince1970 / secondsPerYear)
## Collections ##
Two collection type in Swift, arrays and dictionaries.
1. Arrays
Массив (Array) — это упорядоченная коллекция однотипных элемен- тов, для доступа к которым используются целочисленные индексы .
Arrays hold only one type of value. Every element in the array must be the same type and once an array is declared the type of the elements it holds cannot be changed.Arrays are an ordered list. You can insert elements, delete elements, append elements. 
let names = ["Alice", "Bob", "Carol"]
var ages  = [24, 27, 29]
2. Dictionaries
Словарь — это неупорядоченная коллекция элементов, для доступа к значениям которых используются специальные индексы, называ- емые ключами .
Dictionaries hold key/value pairs. The key is used an index to insert or retrieve the associated value. Dictionaries are not a ordered list but a collection of values and values can only be looked up by key. You can extract a list of values or a list of keys into an Array
let abcAges = ["Alice" : 24, "Bob" : 27, "Carol" : 29]
## Control Flow ##
Control flow statements let you tell the computer what to do next, conditionally with "if" statements, repeatedly looping with "for" statements, or choosing among alternatives with "switch". There are six basic statements:
if \ { ... } else if \ { ... } else { ... }
for \ in \
for ; \; \ { ... }
while \ { ... }
do { ... } while \
switch \ { case \: ..., case \: ..., ... }
### If Statement ###
2 differences: 1. the parentheses () around the conditional expression are optional and can be left out, 2. curly braces { } around the statements are required. If statements can be chained using “else if”.
if cities[0] == "Las Vegas" {
    state = "Nevada"
}

if distanceInMeters < 10 {
    units = Centimeters;
} else if distanceInMeters < 100 {
    units = Meters;
} else {
    units = Kilometers;
} 
###  For Loops ### 
Same 2 differences as the “if” statement: 1. parenthesis around the initialize, condition, and incrementer are optional, 2. curly braces {} around the statements in the loop body are required.
for var i=1; i<=10; ++i {
    // do something using i as it goes from 1 to 10
}
### While Loop Statement ###
var i = 1
while i <= 10 {
    println ("\(i)")
    i++
}
###  Switch Statement ###
1. the “break” at the end of each case is not needed, break is the default
2. the “fallthrough” is required to make a case fall through to the next case
3. the switch must completely cover all values, “default” can be used if necessary
4. the value can be any numeric type (even Float or Double!), an enum, a string or even a Tuple
5. the values in the cases can be ranges (closed or half closed ranges)
6. matching can be used with Tuples, with optional wildcards for values
7. an optional “where” clause can provide additional conditions
