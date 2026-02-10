# JSON Parser

--------

## Overview

This JSON parser:
- Parsing made without Gson or other libs for JSON parsing
- Also conversion: JSON to Java Objects
- File I/O also to dealWithIt.json file

| Component        | Purpose                      | Key Methods                   |
|------------------|------------------------------|-------------------------------|
| **Parser**       | JSON → Java Map/Object       | `JSONIntoMAP()`, `JSONToObj()` |
| **Serializer**   | Java Object → JSON String    | `toJSON()`, `values()`         |
| **File Handler** | Read/Write JSON files        | `FileWriter`                   |

### Key Features

```java
// 1. Parse JSON to Map
Map<String, Object> data = JSONIntoMAP("{\"futureCar\":\"Volvo\"}");

// 2. Convert JSON to Java Object
MyClass obj = JSONToObj(jsonString, MyClass.class);

// 3. Serialize object to JSON
String json = toJSON(obj);

// 4. Save to file
try (FileWriter writer = new FileWriter("dealWithIt.json")) {
    writer.write(toJSON(obj));
}