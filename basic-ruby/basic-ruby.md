# Basic Ruby

## Basic Data Types

- Ruby is strongly object-oriented
  - EVERYTHING IS AN OBJECT
- Four basic data Types
  - numbers (integers and floats)
  - strings
  - symbols
  - booleans

### Lesson Goals

- List basic arithmetic operators
- Describe difference between int and float and conversion between
- Explain string interpolation and concatenation
- Describe escape chars
- Define symbols and how it differs from a string
- Explain Booleans: true, false, nil

### Numbers

- Arithmetic with two integers ALWAYS results in an integer
  - 17 / 5 = 3; not 3.4
- To obtain correct answer, replace an integer w/ float
  - 17 / 5.0 = 3.4
- Converting Number Types
  - Integer -> Float
    - 13.to\_f => 13.0
  - Float -> Integer
    - 13.0.to\_i => 13
- Useful Number Methods
  - #even?
    - 6.even? => true
    - 7.even? => false
  - #odd?
    - 6.odd? => false  
    - 6.odd? => true

### Strings

- Double and Single Quotation Marks
  - Similar but string interpolation and escape characters only work inside DOUBLE QUOTES
- Concatenation
  - Plus Operator
    - "Welcome " + "to " + "Odin" => "Welcome to Odin" 
  - Shovel Operator
    - "Welcome " << "to " << "Odin" => "Welcome to Odin"
  - Concat method
    - "Welcome ".concat("to ").concat("Odin") => "Welcome to Odin"
- Substrings
  - "hello"[0] => "h"
  - "hello"[0..1] => "he"
  - "hello"[0, 4] => "hell"
  - "hello"[-1] => "o"
- Escape Characters
  - Esc chars are representation of whitespace chars and allow for quotation marks as part of string
  - Only work inside double quotes
  - \\ => Backslash in string
  - \b => Backspace
  - \r => Carriage return
  - \n => Newline
  - \s => Space
  - \t => Tab
  - \" => Double quotation mark
  - \' => Single quotation mark 
- Interpolation
  - Allows you to evaluate string that contains placeholder variables
  - Only works double quotes
  
`
name = "Odin"

puts "Hello, #{name}" # => "Hello, Odin"
puts 'Hello, #{name}' # => "Hello, #{name}"
`

- Common String Methods
  - #capitalize
   `"hello".capitalize # => "Hello`
  - #include?
    `"hello".include?("lo") # => true`
  - #upcase
    `"hello".upcase #=> "HELLO"`
  - #downcase
    `"Hello".downcase #=> "hello"`
  - #empty?
    `"hello".empty? #=> false`
  - #length
    `"hello".length #=> 5`
  - #reverse
    `"hello".reverse #=> "olleh"`
  - #split
    `"hello world".split #=> ["hellow", "world"]`
  - #strip
    `" hello, world   ".strip #=> "hello, world`
- Converting other objects to strings
  - to\_s
    `5.to_s #=> "5"`
    `nil.to_s #=> ""`

### Symbols

- Symbols differ from strings in that they are only stored in memory once, making them faster
- Common application of symbols are hash keys
- Create a symbol
  `:my_symbol`
- Symbols vs. Strings
  `
  "string" == "string" #=> true
  "string".object_id == "string".object_id #=> false
  :symbol.object_id == :symbol.object_id #=> true
  `

### Booleans

- True, False blah blah
- Nil
  - null value
