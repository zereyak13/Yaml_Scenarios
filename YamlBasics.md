# Yaml
YAML is a human-readable data serialization language. It is often used for configuration files, but it can be used for a wide variety of applications, including data exchange and object serialization.

Here are some key features and concepts that you should understand when learning YAML basics:
- Yaml Syntax
- Data Types
- Comments
- Anchors and Aliases
- YAML Document Structure
- YAML Indentation

#### YAML Syntax
YAML uses a simple and human-readable syntax that is based on indentation and whitespace. YAML documents are structured using blocks of text that are separated by whitespace. Blocks are indented to show hierarchy and structure, similar to how code is indented in programming languages. Here are some examples of YAML syntax:
##### Scalars:
Scalars are single values in YAML, such as strings, numbers, and booleans. Here's an example of a string scalar:
```sh
name: John Doe
```
##### Lists: 
Lists are collections of values in YAML, enclosed in square brackets. Here's an example of a list:
```sh
fruits:
  - apple
  - banana
  - orange
```
##### Maps: 
Maps are collections of key-value pairs in YAML, enclosed in curly braces. Here's an example of a map:
```sh
person:
  name: John Doe
  age: 30
  address:
    street: 123 Main St
    city: Anytown
    state: CA
```
In this example, "person" is the key and the value is a map containing the person's name, age, and address.

##### Nested Structures:
YAML allows you to nest lists and maps within each other. Here's an example of a nested map:
```sh
employees:
  - name: John Doe
    title: Manager
    department: Sales
  - name: Jane Smith
    title: Engineer
    department: IT
```
In this example, "employees" is a key with a list of maps as its value. Each map represents an employee with their name, title, and department.
##### Comments: 
YAML allows you to add comments to your code using the "#" symbol. Here's an example of a commented YAML file:
```sh
# This is a YAML file with comments

# Person information
person:
  name: John Doe # The person's name
  age: 30 # The person's age

# Address information
address:
  street: 123 Main St # The street address
  city: Anytown # The city
  state: CA # The state
```
In this example, "#" is used to add comments to the YAML file, providing additional information and context for the data.

##### Anchors and Aliases:
YAML supports the use of anchors and aliases to create references to other parts of your code. An anchor is a named reference to a piece of code, while an alias is a reference to that anchor. This can be useful for reducing duplication in your code. Here is an example of using anchors and aliases in YAML:
```sh
# This is a YAML file with comments

# Person information
person:
  name: John Doe # The person's name
  age: 30 # The person's age

# Address information
address:
  street: 123 Main St # The street address
  city: Anytown # The city
  state: CA # The state
```
In this example, we are using anchors and aliases to define a set of default values for a production and staging environment. The &defaults is used to define an anchor that references the default values. The <<: *defaults syntax is used to include all the values defined in the defaults anchor into the current mapping.

So, both the production and staging environments inherit the timeout and retries values from the defaults anchor. 

##### YAML Document Structure:
YAML documents are structured using a series of key-value pairs. Each key-value pair is separated by a colon and can be followed by a space and a value. Keys must be unique within a document and are case-sensitive.
```sh
---
name: John Doe
age: 30
address:
  street: 123 Main St
  city: Anytown
  state: CA
---
name: Jane Smith
age: 25
address:
  street: 456 Elm St
  city: Another Town
  state: NY
```
In this example, we have two YAML documents separated by a --- separator. Each document is a collection of key-value pairs and is structured using YAML syntax.

The first document represents a person named John Doe with their age and address. The second document represents a person named Jane Smith with their age and address. Both documents use the same structure and syntax, with keys and values separated by a colon and nested structures using indentation.

By separating the documents with the --- separator, we can have multiple YAML documents in a single file, each representing different data structures or entities. This can be useful for organizing data in a single file, or for representing data from different sources or systems.

##### YAML Indentation: 
YAML uses indentation to indicate hierarchy and structure. Indentation is typically two or four spaces, although any consistent amount of whitespace can be used. Blocks that are at the same level of indentation are considered to be at the same level of hierarchy. Here is an example of YAML indentation:
```sh
fruits:
    apple:
        color: red
        price: 0.50
    banana:
        color: yellow
        price: 0.25
```
In this example, we have a map with two key-value pairs, "apple" and "banana". Each key has a nested map with two key-value pairs, "color" and "price". The indentation is used to indicate the nesting of the key-value pairs.

In YAML, each level of indentation is represented by two or more spaces (or a single tab character, although spaces are recommended for consistency). The indentation is used to indicate the hierarchy of the data structure, similar to how curly braces are used in other languages like JSON.

In this example, the "apple" and "banana" keys are indented by four spaces to indicate that they are nested within the "fruits" key. The "color" and "price" keys are indented by eight spaces to indicate that they are nested within the "apple" and "banana" keys.

It's important to note that YAML is sensitive to indentation, and improper indentation can lead to errors or unexpected results. It's recommended to use a consistent indentation style throughout a YAML file to ensure readability and consistency.

>These are the basic concepts that you should understand when learning YAML. Once you have a good understanding of these concepts, you can start to use YAML for a variety of applications, including configuration files, data exchange, and object serialization.
