# Yaml-datatypes

### YAML: 
It was first called Yet Another MarkUp Langugae but now it is Yaml Ain't MarkUp Language.
### Definition:
Applications written with different technologies or languages which have different *Data Structures* can transfer data to each other using a *Common/ Standerd Format*. YAML, JSON and XML are these formats

It is a Data Serialization Language
 - Data Serialization:
Translation of Object (Code + Data) into stream of bytes that saves the state of this object in a form that is transmittable. Using Serialization, data can be converted into code and code can be converted into data again.

Benifits of YAML:
- Simple and easy to read
- Nice and Strict Syntax
- Most Languages use it
- More powerful when representing complex data


##### Yaml Automatically Determines the data type if not specified

```
name: Rahul
age: 24
job: no
```

#### But you can specify a dataType
```
Syntax --> variable: !!datatype value
age: !!int 22
```

#### Some Common are
```
zero: !!int 0
positiveNum: !!int 9
negativeNum: !!int -9
commaValue: !!int 255_000 #255,000
```

#### Other Types
```
PI: !!float 3.14
infinite: !!infinite .inf
not a num: !!nan .nan
booleanValue: !!boolean no
nameString: !!str Rahul
nullDataType: !!null null #null or NULL or ~
```

#### Lists
```
- Item1
- Item2
- Item3
```

#### Nested Lists
```
-
 - Item1
 - Item2
 - Item3

-
 - Item1
 - Item2
 - Item3
```
