# Regex Cheat Sheet
--- 
Regular expressions (regex) are a powerful tool for finding, matching, and manipulating text based on patterns. This guide covers the basics, key symbols, and common uses for regex. Whether you're processing logs, validating inputs, or extracting data, regex is extremely useful.


## Table of Contents
1. [Basic Symbols](#1-basic-symbols)
2. [Character Classes](#2-character-classes)
3. [Quantifiers](#3-quantifiers)
4. [Grouping and Alternation](#4-grouping-and-alternation)
5. [Anchors](#5-anchors)
6. [Lookahead and Lookbehind (Advanced)](#6-lookahead-and-lookbehind-advanced)
7. [Examples](#7-examples)

---

## 1. **Basic Symbols**

- `.`: **Matches any character** except new lines.  
  Example: `a.b` will match `acb`, `a1b`, etc., but not `ab`.

- `^`: **Matches the beginning of the string**.  
  Example: `^hello` will only match "hello" if it’s at the start.

- `$`: **Matches the end of the string**.  
  Example: `world$` will only match "world" if it’s at the end.

- `\`: **Escape character**. Use it before special symbols to match them literally.  
  Example: `\.` matches a literal period (.), not any character.

---

## 2. **Character Classes**

Character classes help you match specific types of characters.

- `[ ]`: **Matches any one of the characters inside** the square brackets.  
  Example: `[aeiou]` matches any vowel: `a`, `e`, `i`, `o`, `u`.

- `[^ ]`: **Matches any character that is NOT inside** the square brackets.  
  Example: `[^aeiou]` matches any consonant.

- `\d`: **Matches any digit** (0–9).  
  Example: `\d` matches `1`, `2`, `3`, etc.

- `\D`: **Matches anything that's not a digit**.  
  Example: `\D` matches letters or symbols.

- `\w`: **Matches any "word character"** (letters, numbers, or underscores).  
  Example: `\w` matches `a`, `A`, `1`, `_`.

- `\W`: **Matches anything that is not a "word character"**.  
  Example: `\W` matches spaces, punctuation, etc.

- `\s`: **Matches any whitespace character** (like spaces, tabs, etc.).

- `\S`: **Matches anything that is not whitespace**.

---

## 3. **Quantifiers**

Quantifiers tell you **how many times** to match a character or group.

- `*`: **Matches 0 or more** of the previous character.  
  Example: `a*b` matches `b`, `ab`, `aaab`.

- `+`: **Matches 1 or more** of the previous character.  
  Example: `a+b` matches `ab`, `aaab`, but not `b`.

- `?`: **Matches 0 or 1** of the previous character.  
  Example: `colou?r` matches both `color` and `colour`.

- `{n}`: **Matches exactly n occurrences** of the previous character.  
  Example: `\d{4}` matches exactly `2025`.

- `{n,}`: **Matches n or more occurrences** of the previous character.  
  Example: `\d{2,}` matches `12`, `123`, etc.

- `{n,m}`: **Matches between n and m occurrences** of the previous character.  
  Example: `\d{2,4}` matches `12`, `123`, or `1234`.

---

## 4. **Grouping and Alternation**

You can group parts of your regex or choose between options.

- `( )`: **Groups characters together**.  
  Example: `(abc)+` matches `abc`, `abcabc`, etc.

- `|`: **OR operator** – matches one thing or another.  
  Example: `cat|dog` matches either `cat` or `dog`.

---

## 5. **Anchors**

Anchors let you specify where to match in the string.

- `\b`: **Matches a word boundary** (beginning or end of a word).  
  Example: `\bcat\b` will match "cat" in "cat is here", but not in "scattered".

- `\B`: **Matches non-word boundaries** (not at the start or end of a word).  
  Example: `\Bcat\B` will match `scat` in `scatter`, but not `cat`.

---

## 6. **Lookahead and Lookbehind (Advanced)**

Lookahead and lookbehind check for things **before** or **after** the current position.

- `(?= )`: **Positive lookahead** – matches if something comes **after**.  
  Example: `\d(?=\D)` matches a digit only if it’s followed by a non-digit.

- `(?! )`: **Negative lookahead** – matches if something **does not follow**.  
  Example: `\d(?!\D)` matches a digit only if it’s not followed by a non-digit.

- `(?<= )`: **Positive lookbehind** – matches if something comes **before**.  
  Example: `(?<=@)\w+` matches the domain in `user@example.com` (`example`).

- `(?<! )`: **Negative lookbehind** – matches if something **does not come before**.  
  Example: `(?<!@)\w+` matches a word unless it’s preceded by `@`.

---

## 7. **Examples**

- **Match a Date (YYYY-MM-DD)**:  
  `\d{4}-\d{2}-\d{2}`  
  Example: `2025-01-01`

- **Match a Phone Number (e.g., `123-456-7890`)**:  
  `\d{3}-\d{3}-\d{4}`  
  Example: `123-456-7890`

- **Match an Email Address**:  
  `\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}\b`  
  Example: `user@example.com`

- **Match a URL**:  
  `https?://[a-zA-Z0-9.-]+(?:/[a-zA-Z0-9.-]*)*`  
  Example: `http://example.com`

- **Match an IP Address**:  
  `\d{1,3}(\.\d{1,3}){3}`  
  Example: `192.168.1.1`

---

## 8. **Helpful Resources**

- [Regex101](https://regex101.com/) – Test and debug your regex patterns.
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) – Beginner-friendly guide to regex.

---

Happy regex-ing! 😄
