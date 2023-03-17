# Yaml
In the previous lesson, we learned about the YAML syntax. In this lesson, we will focus on the data types that make up YAML syntax.

#### YAML Data Types
In YAML, data types are used to represent different kinds of data in a structured way. They define the format and structure of the data being represented in the YAML document.

For example, YAML has several built-in data types, such as scalars (strings, integers, booleans, and null values), sequences (ordered lists of items), and maps (key-value pairs).

By using data types in YAML, we can create well-structured and organized documents that are easy to read and parse. This makes it a useful format for storing and exchanging data between different applications and programming languages. Additionally, data types can help ensure that the data being represented in the YAML document is valid and conforms to a certain structure, which can be helpful for debugging and preventing errors in applications that use the data.
- Scalars - simple values like strings, numbers, and booleans.
- Sequences - lists of values, represented using hyphens to indicate each item in the list.
- Maps - collections of key-value pairs, represented using the key-value syntax with indentation to indicate nesting.
- Null - a special value that represents the absence of a value.
- Timestamps - date and time values, represented using the ISO 8601 format.
- Anchors and aliases - used to reference and reuse values within the same YAML document.

##### Scalars:
Scalars in YAML are simple values like strings, numbers, and booleans. They are called "scalars" because they represent a single value, as opposed to a collection of values like a sequence or a map.

YAML supports several scalar types, including:

- Strings - which can be enclosed in single or double quotes. YAML also allows for plain scalars, which are unquoted strings that do not contain any special characters like spaces or punctuation.
- Numbers - which can be integers or floating-point values, and can also be expressed in scientific notation.
- Booleans - represented as "true" or "false".
- Null - a special value that represents the absence of a value.
- Here is an example YAML document that demonstrates the use of scalar values.

Here is an example YAML document that demonstrates the use of scalar values
```sh
name: "Alice"
age: 25
is_student: true
favorite_numbers:
  - 3.14
  - 42
```
In this example, "name" is a string scalar, "age" is an integer scalar, "is_student" is a boolean scalar, and "favorite_numbers" is a sequence of two scalar values: a float and an integer.

Scalars can be used as values for keys in maps, as elements in sequences, or as standalone values. They can also be combined with other YAML features like anchors and aliases to create more complex data structures.
##### Sequences: 
Sequences in YAML represent lists of values, and are indicated using hyphens (-) at the beginning of each item in the list. Sequences can contain any combination of scalar values or complex structures like maps or sequences.

Here's an example YAML document that demonstrates the use of sequences:
```sh
fruits:
  - apple
  - banana
  - cherry
```
In this example, "fruits" is a map with a single key, and the value associated with the "fruits" key is a sequence of three string values: "apple", "banana", and "cherry".

Sequences can also be nested within other sequences, like this:
```sh
- name: Alice
  favorite_fruits:
    - apple
    - banana
- name: Bob
  favorite_fruits:
    - cherry
    - peach
```
Here's an example of a more complex sequence in YAML, which uses a sequence of maps to represent a list of books with various attributes:
```sh
- title: "The Hitchhiker's Guide to the Galaxy"
  author: "Douglas Adams"
  publication_date: 1979
  genres:
    - science fiction
    - humor
  characters:
    - Arthur Dent
    - Ford Prefect
    - Zaphod Beeblebrox

- title: "To Kill a Mockingbird"
  author: "Harper Lee"
  publication_date: 1960
  genres:
    - novel
    - bildungsroman
  characters:
    - Scout Finch
    - Atticus Finch
    - Jem Finch
```
In this example, we have a sequence of two maps, each representing a book. Each book map contains several keys:

"title": the title of the book, represented as a string scalar.
"author": the author of the book, represented as a string scalar.
"publication_date": the publication date of the book, represented as an integer scalar.
"genres": a sequence of string values representing the genres of the book.
"characters": a sequence of string values representing the main characters in the book.
The use of sequences of maps in this example allows for a rich and expressive representation of complex data, and demonstrates the power and flexibility of YAML's sequence data type.

##### Maps: 
Maps in YAML are collections of key-value pairs, similar to dictionaries or hashes in other programming languages. Maps are indicated by a colon (:) separating the key and value, and each key-value pair is separated by a newline. Maps can contain any combination of scalar values or complex structures like sequences or nested maps.

Here's an example YAML document that demonstrates the use of maps:
```sh
person:
  name: Alice
  age: 25
  address:
    street: 123 Main St.
    city: Anytown
    state: CA
    zip: 12345
```
In this example, "person" is a map with three keys: "name", "age", and "address". The value associated with the "name" key is a string scalar ("Alice"), the value associated with the "age" key is an integer scalar (25), and the value associated with the "address" key is a nested map with four keys: "street", "city", "state", and "zip". Each of these keys has a string scalar value.

Maps can also be used to represent more complex data structures, like this:
```sh
employees:
  - name: Alice
    age: 25
    title: Software Engineer
  - name: Bob
    age: 30
    title: Senior Engineer
    projects:
      - Project A
      - Project B
      - Project C
```
In this example, we have a map with a single key "employees", which has a value that is a sequence of two maps. Each map in the sequence represents an employee, with keys for "name", "age", and "title". The second employee also has a key for "projects", which is a sequence of string values.

Overall, maps in YAML are a powerful tool for representing complex data structures, and can be used in a wide range of applications.

##### Null:
In YAML, "null" is a special value that represents the absence of a value. It is often used to indicate that a value is unknown or undefined, or to explicitly clear the value of a variable or field.

In YAML, "null" is represented using the special keyword "null" or "~". Here's an example of how null can be used in YAML:
```sh
person:
  name: Alice
  age: null
```
In this example, "person" is a map with two keys: "name" and "age". The value associated with the "name" key is a string scalar ("Alice"), but the value associated with the "age" key is "null", indicating that we don't know or haven't specified Alice's age.

Here another examle for null value:
```sh
list:
  - item 1
  - null
  - item 3
```
##### Timestamps: 
In YAML, timestamps can be used to represent points in time. Timestamps can be expressed in several formats, including ISO 8601 and RFC 3339.

Here's an example of a timestamp in YAML using ISO 8601 format:
```sh
date: 2022-02-28T13:45:00Z
```
In this example, the key "date" has a value that represents a specific point in time, February 28th, 2022 at 1:45 PM UTC. The "T" character separates the date and time components, and the "Z" at the end indicates that the time is in UTC (Coordinated Universal Time).
In this example, "#" is used to add comments to the YAML file, providing additional information and context for the data.

YAML timestamps can also include a fraction of a second, indicated by a decimal point and one or more digits after the second component:
```sh
time: 2022-02-28T13:45:00.123456Z
```
In this example, the key "time" represents a more precise point in time, with a fraction of a second included in the timestamp.

Timestamps in YAML can also include a time zone offset, indicated by a plus or minus sign followed by the number of hours and minutes offset from UTC:
```sh
datetime: 2022-02-28T13:45:00-05:00
```
In this example, the key "datetime" represents a point in time on February 28th, 2022 at 1:45 PM Eastern Standard Time (EST), which is 5 hours behind UTC.

Overall, timestamps in YAML are a useful tool for representing time-based data and can be used in a wide range of applications.

##### Anchors and Aliases:
 In YAML, anchors and aliases are a way to reuse data across a document or within a data structure.

An anchor is a unique identifier that can be assigned to any node in a YAML document by prefixing it with an ampersand (&) followed by the anchor name. For example:
```sh
person: &alice
  name: Alice
  age: 30
```
In this example, the "person" node is assigned the anchor name "alice". This means that we can later reference this node using an alias, which is a reference to the anchor name prefixed by an asterisk (*). For example:
```sh
other_person:
  name: Bob
  spouse: *alice
```
In this example, the "spouse" key in the "other_person" map is set to an alias to the "alice" anchor. This means that the "spouse" key will have the same value as the "person" node defined earlier in the document.

Using anchors and aliases can be particularly useful when working with complex data structures or when multiple parts of a document share the same data. By defining data once and referencing it with aliases, YAML documents can be more concise and easier to read.

Note that anchors and aliases can only reference nodes that have already been defined in the YAML document, and that aliases cannot be used outside of the document where their anchor was defined.