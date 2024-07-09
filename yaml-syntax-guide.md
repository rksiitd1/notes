# YAML Syntax: A Comprehensive Guide

YAML (YAML Ain't Markup Language) is a human-friendly data serialization standard. It's commonly used for configuration files and in applications where data is being stored or transmitted. This guide will walk you through the essentials of YAML syntax.

## 1. Basic Structure

YAML uses indentation with spaces to denote structure. Never use tabs.

```yaml
key: value
nested_key:
  sub_key: sub_value
```

## 2. Scalars (Strings, Numbers, Booleans)

Strings:
```yaml
unquoted: Hello World
single_quoted: 'Hello ''World'''
double_quoted: "Hello \"World\""
multi_line: |
  This is a multi-line
  string
folded: >
  This is a folded
  string
```

Numbers and Booleans:
```yaml
integer: 42
float: 3.14159
boolean: true
also_boolean: yes
```

## 3. Lists

```yaml
- item1
- item2
- item3

nested_list:
  - nested_item1
  - nested_item2
```

## 4. Dictionaries (Hash Tables)

```yaml
key1: value1
key2: value2

nested_dict:
  key3: value3
  key4: value4
```

## 5. Combining Lists and Dictionaries

```yaml
employees:
  - name: John Doe
    age: 30
    position: Developer
  - name: Jane Smith
    age: 28
    position: Designer
```

## 6. Anchors and Aliases

Anchors (&) define a chunk of configuration, and aliases (*) reference it:

```yaml
defaults: &defaults
  timeout: 30
  retries: 3

development:
  <<: *defaults
  server: dev.example.com

production:
  <<: *defaults
  server: prod.example.com
```

## 7. Multiple Documents

Use `---` to separate multiple documents in a single file:

```yaml
---
document: 1
---
document: 2
```

## 8. Comments

Use the `#` symbol for comments:

```yaml
# This is a comment
key: value  # This is an inline comment
```

## 9. Explicit Data Types

YAML can explicitly specify data types:

```yaml
integer: !!int 42
float: !!float 3.14
string: !!str 42
boolean: !!bool true
null: !!null null
datetime: !!timestamp 2023-01-01T12:00:00Z
```

## 10. Complex Mapping Keys

You can use complex structures as keys:

```yaml
? - key1
  - key2
: value
```

## Best Practices

1. Use consistent indentation (2 spaces is common).
2. Prefer explicit truthy/falsy values (`true`/`false` over `yes`/`no`).
3. Use quotes for strings containing special characters.
4. Leverage anchors and aliases to reduce repetition.
5. Always validate your YAML using a linter.

## Common Pitfalls

1. Mixing tabs and spaces for indentation.
2. Forgetting to quote strings that start with special characters.
3. Incorrect use of multi-line string syntax.
4. Inconsistent indentation levels.

YAML's simplicity makes it readable and writable, but attention to detail is crucial. Always refer to the [official YAML specification](https://yaml.org/spec/1.2.2/) for the most up-to-date and comprehensive information.
