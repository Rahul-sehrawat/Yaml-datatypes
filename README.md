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

#### Block Type / Object
```
ObjectTypeKeyValue:
  KeyValue: Pair
  KeyValue2: Pair2
```

#### Or

```
ObjectTypeSimpleList: -Item1
  -Item2
  -Item3
```

#### You want to display multiple line in your browser but you want your browser to treat it as a single line #Use ">"
```
aboutInSingleLine: >-
  My name is Rahul Sehrawat
  Right Now i am Learning DevOps
  and Full Stack Dev
```

#### Same as
```
about2: My name is Rahul Sehrawat Right Now i am Learning DevOps and Full Stack Dev
```

#### Remember Indentation (one space) is very important here
```
aboutTwoMultipleLine: |-
  My name is Rahul Sehrawat
  Right Now i am Learning DevOps
  and Full Stack Dev
```

#### Single Key but have two Values
```
pairExample: 
  - job: Student
  - job: Teacher
```

#### Set
```
SetExample:
?Rahul: Student
?Rue: Unknown
?Luffy: Pirate
```

#### Dictionary
```
People:
 -Rahul:
  - Role: Student
  - Age: 24
 -Luffy:
  -Role: Pirate
  -Age: 19
```

#### Reusing Properties
```
Likes: &likes
 - Sport: Cricket
 - Food: pizza

Person1:
 -Name: Rahul
 <<: *likes
```
