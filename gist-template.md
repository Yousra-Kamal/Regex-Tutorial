# Regular Expression - Matching a URL

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. In this tutorial we'll see how to use a regex to match a URL.

## Summary

In this tutorial I'll be covering and breaking down the components of a regular expression used to match and validate URLs:

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

## Table of Contents

- [Regular Expression - Matching a URL](#regular-expression---matching-a-url)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [🌻 Regex Components](#-regex-components)
    - [◾ Anchors](#-anchors)
    - [◾ Quantifiers](#-quantifiers)
    - [◾ Grouping Constructs](#-grouping-constructs)
    - [◾ Bracket Expressions](#-bracket-expressions)
  - [🌻 Matching a URL](#-matching-a-url)
    - [1-Protocol](#1-protocol)
    - [2-Domain Name](#2-domain-name)
    - [3-Top-Level Domain](#3-top-level-domain)
    - [4-Path and File Name](#4-path-and-file-name)
  - [Author](#author)

## 🌻 Regex Components

### ◾ Anchors


The URL matching regex starts with the `^` (caret) symbol and ends with the  `$` (dollar) symbol. These anchors define that the entire string must match the pattern between them, ensuring that the regex matches the complete URL and not just a part of it.

- The caret anchor indicates that the string to be examined must include the characters following it. It is important to note that the regular expression is case-sensitive.
- The dollar sign anchor indicates that the string to be examined includes the characters preceding it.

### ◾ Quantifiers

 Quantifiers used to quantify how many times a part of your regular expression should be repeated.
- `*` (zero or more occurrences)
- `+` (one or more occurrences)
- `?` (zero or one occurrence)
- `{}` (specifying a specific range of occurrences).

### ◾ Grouping Constructs

The parentheses grouping constructs `()` in regular expressions are used to group commands together to determine the order of processing.

### ◾ Bracket Expressions
Bracket Expressions `[]` match any one of a set of characters specified within square brackets.
For example, [abc] matches any single character that is either a, b, or c.

## 🌻 Matching a URL

```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

### 1-Protocol
This part of our regex `https?:\/\/` matches the protocol of a URL, such as "http://" or "https://". The `?` makes the 's' character optional, allowing URLs with both HTTP and HTTPS protocols to match.


### 2-Domain Name
This section `[\da-z.-]+` matches the domain name in the URL. It allows for alphanumeric characters (including digits), hyphens, and dots.
- `www.example`


### 3-Top-Level Domain
This section `[a-z.]{2,6}` matches the top-level domain part of the URL.
It typically includes domain extensions like .com, .net, .org, etc. The {2,6} specifies that it can consist of 2 to 6 characters.

- `.com`
- `.org`


### 4-Path and File Name
This segment `[/\w .-]*` matches the path and file name portion of the URL(represents the specific location or resource on the web server). It allows forward slashes, word characters, spaces, dots, and hyphens.
- `/page1.html`


## Author

Yousra Kamal a software developer student with a bachelors degree in clinical pharmacy looking to succeed and dominate the web. 

GitHub: [Yousra-Kamal](https://github.com/Yousra-Kamal)