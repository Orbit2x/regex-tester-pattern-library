# Regex Tester & Pattern Library - 40+ Prebuilt Regular Expressions

[![Regex Tester](https://img.shields.io/badge/Try%20Online-Regex%20Tester-blue)](https://orbit2x.com/regex-tester)
[![Regex Library](https://img.shields.io/badge/Library-40%2B%20Patterns-green)](https://orbit2x.com/regex-library)

> **Testing regular expressions?** Try the free [Regex Tester at Orbit2x](https://orbit2x.com/regex-tester) with live matching and syntax highlighting. Or browse [40+ prebuilt patterns](https://orbit2x.com/regex-library) for common tasks.

## Quick Access

- 🧪 **[Regex Tester](https://orbit2x.com/regex-tester)** - Live regex testing with match highlighting
- 📚 **[Regex Library](https://orbit2x.com/regex-library)** - 40+ ready-to-use patterns for email, URL, phone, etc.
- 🔍 **[Grep Tool](https://orbit2x.com/grep)** - Search text with regex patterns

---

## Most Common Regex Patterns

### Email Validation

```regex
# Basic email (99% cases)
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$

# RFC 5322 compliant (more strict)
^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?)*$
```

**Test online**: [Regex Tester](https://orbit2x.com/regex-tester)

### URL Validation

```regex
# HTTP/HTTPS URLs
^https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)$

# URLs with optional protocol
^(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)$
```

### Phone Numbers (US)

```regex
# (123) 456-7890 or 123-456-7890
^\(?([0-9]{3})\)?[-.\s]?([0-9]{3})[-.\s]?([0-9]{4})$

# International format (+1 123 456 7890)
^\+?([0-9]{1,3})\s?([0-9]{3})\s?([0-9]{3})\s?([0-9]{4})$
```

### IP Addresses

```regex
# IPv4 (0.0.0.0 to 255.255.255.255)
^((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$

# IPv6
^(([0-9a-fA-F]{1,4}:){7}[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,7}:|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})|:((:[0-9a-fA-F]{1,4}){1,7}|:)|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]|(2[0-4]|1{0-1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9]))$
```

### Dates

```regex
# YYYY-MM-DD
^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])$

# DD/MM/YYYY or MM/DD/YYYY
^(0[1-9]|[12][0-9]|3[01])[\/](0[1-9]|1[0-2])[\/]\d{4}$
```

### Credit Cards

```regex
# Visa (starts with 4)
^4[0-9]{12}(?:[0-9]{3})?$

# MasterCard (starts with 51-55 or 2221-2720)
^5[1-5][0-9]{14}$|^2(?:2(?:2[1-9]|[3-9][0-9])|[3-6][0-9][0-9]|7(?:[01][0-9]|20))[0-9]{12}$

# American Express (starts with 34 or 37)
^3[47][0-9]{13}$
```

**Browse all patterns**: [Regex Library with 40+ Patterns](https://orbit2x.com/regex-library)

---

## Using Regex in Different Languages

### JavaScript

```javascript
// Test if string matches pattern
const email = "user@example.com";
const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

if (emailRegex.test(email)) {
  console.log("✅ Valid email");
} else {
  console.log("❌ Invalid email");
}

// Extract matches
const text = "Contact us at support@example.com or sales@example.com";
const matches = text.match(/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/g);
console.log(matches);
// ["support@example.com", "sales@example.com"]

// Replace with regex
const cleaned = text.replace(/@example\.com/g, "@newdomain.com");

// Capture groups
const urlRegex = /^(https?):\/\/([^\/]+)(\/.*)?$/;
const url = "https://example.com/path/page";
const [, protocol, domain, path] = url.match(urlRegex);
console.log({ protocol, domain, path });
// { protocol: 'https', domain: 'example.com', path: '/path/page' }
```

### Python

```python
import re

# Test if string matches
email = "user@example.com"
email_regex = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'

if re.match(email_regex, email):
    print("✅ Valid email")
else:
    print("❌ Invalid email")

# Find all matches
text = "Contact us at support@example.com or sales@example.com"
matches = re.findall(r'[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}', text)
print(matches)
# ['support@example.com', 'sales@example.com']

# Replace with regex
cleaned = re.sub(r'@example\.com', '@newdomain.com', text)

# Capture groups
url_regex = r'^(https?):\/\/([^\/]+)(\/.*)?$'
url = "https://example.com/path/page"
match = re.match(url_regex, url)
if match:
    protocol, domain, path = match.groups()
    print(f"Protocol: {protocol}, Domain: {domain}, Path: {path}")
```

### PHP

```php
<?php
// Test if string matches
$email = "user@example.com";
$emailRegex = '/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/';

if (preg_match($emailRegex, $email)) {
    echo "✅ Valid email\n";
} else {
    echo "❌ Invalid email\n";
}

// Find all matches
$text = "Contact us at support@example.com or sales@example.com";
preg_match_all('/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/', $text, $matches);
print_r($matches[0]);
// Array ( [0] => support@example.com [1] => sales@example.com )

// Replace with regex
$cleaned = preg_replace('/@example\.com/', '@newdomain.com', $text);

// Capture groups
$urlRegex = '/^(https?):\/\/([^\/]+)(\/.*)?$/';
$url = "https://example.com/path/page";
if (preg_match($urlRegex, $url, $matches)) {
    echo "Protocol: {$matches[1]}, Domain: {$matches[2]}, Path: {$matches[3]}\n";
}
?>
```

### Go

```go
package main

import (
    "fmt"
    "regexp"
)

func main() {
    // Test if string matches
    email := "user@example.com"
    emailRegex := regexp.MustCompile(`^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`)

    if emailRegex.MatchString(email) {
        fmt.Println("✅ Valid email")
    } else {
        fmt.Println("❌ Invalid email")
    }

    // Find all matches
    text := "Contact us at support@example.com or sales@example.com"
    pattern := regexp.MustCompile(`[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}`)
    matches := pattern.FindAllString(text, -1)
    fmt.Println(matches)
    // [support@example.com sales@example.com]

    // Replace with regex
    cleaned := pattern.ReplaceAllString(text, "REDACTED")

    // Capture groups
    urlRegex := regexp.MustCompile(`^(https?):\/\/([^\/]+)(\/.*)?$`)
    url := "https://example.com/path/page"
    groups := urlRegex.FindStringSubmatch(url)
    if len(groups) > 0 {
        fmt.Printf("Protocol: %s, Domain: %s, Path: %s\n", groups[1], groups[2], groups[3])
    }
}
```

---

## Regex Cheat Sheet

### Character Classes

| Pattern | Matches | Example |
|---------|---------|---------|
| `.` | Any character except newline | `a.c` matches "abc", "a1c" |
| `\d` | Any digit (0-9) | `\d{3}` matches "123" |
| `\D` | Any non-digit | `\D+` matches "abc" |
| `\w` | Word character (a-z, A-Z, 0-9, _) | `\w+` matches "hello_123" |
| `\W` | Non-word character | `\W+` matches "!@#" |
| `\s` | Whitespace (space, tab, newline) | `\s+` matches "   " |
| `\S` | Non-whitespace | `\S+` matches "hello" |
| `[abc]` | Any of a, b, or c | `[aeiou]` matches vowels |
| `[^abc]` | Not a, b, or c | `[^0-9]` matches non-digits |
| `[a-z]` | Range a to z | `[A-Z]+` matches "HELLO" |

### Quantifiers

| Pattern | Matches | Example |
|---------|---------|---------|
| `*` | 0 or more | `a*` matches "", "a", "aaa" |
| `+` | 1 or more | `a+` matches "a", "aaa" |
| `?` | 0 or 1 | `colou?r` matches "color", "colour" |
| `{n}` | Exactly n | `\d{3}` matches "123" |
| `{n,}` | n or more | `\d{3,}` matches "123", "1234" |
| `{n,m}` | n to m | `\d{2,4}` matches "12", "123", "1234" |

### Anchors

| Pattern | Matches | Example |
|---------|---------|---------|
| `^` | Start of string | `^Hello` matches "Hello world" |
| `$` | End of string | `world$` matches "Hello world" |
| `\b` | Word boundary | `\bcat\b` matches "cat" not "catch" |
| `\B` | Non-word boundary | `\Bcat\B` matches "concatenate" |

### Groups

| Pattern | Purpose | Example |
|---------|---------|---------|
| `(abc)` | Capture group | `(\d{3})-(\d{4})` captures "123-4567" |
| `(?:abc)` | Non-capturing group | `(?:https?):\/\/` |
| `(a\|b)` | Alternation (OR) | `(cat\|dog)` matches "cat" or "dog" |
| `(?=abc)` | Positive lookahead | `\d+(?= dollars)` matches "10" in "10 dollars" |
| `(?!abc)` | Negative lookahead | `\d+(?! dollars)` |

**Practice with**: [Regex Tester](https://orbit2x.com/regex-tester)

---

## Common Regex Tasks

### 1. Extract Domain from Email

```javascript
const email = "user@example.com";
const domain = email.match(/@(.+)$/)[1];
console.log(domain); // "example.com"
```

### 2. Validate Password Strength

```regex
# At least 8 chars, 1 uppercase, 1 lowercase, 1 number, 1 special char
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$
```

### 3. Extract Hashtags

```javascript
const tweet = "Learning #regex is fun! #coding #javascript";
const hashtags = tweet.match(/#\w+/g);
console.log(hashtags); // ["#regex", "#coding", "#javascript"]
```

### 4. Remove HTML Tags

```javascript
const html = "<p>Hello <strong>world</strong></p>";
const text = html.replace(/<[^>]*>/g, "");
console.log(text); // "Hello world"
```

### 5. Validate Hex Color

```regex
# #RGB or #RRGGBB
^#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$
```

### 6. Extract All Numbers

```javascript
const text = "I have 5 apples and 10 oranges";
const numbers = text.match(/\d+/g);
console.log(numbers); // ["5", "10"]
```

### 7. Camel Case to Snake Case

```javascript
const camelCase = "myVariableName";
const snakeCase = camelCase.replace(/([A-Z])/g, "_$1").toLowerCase();
console.log(snakeCase); // "my_variable_name"
```

### 8. Validate Credit Card (Luhn Algorithm + Regex)

```regex
# Visa, MasterCard, Amex, Discover
^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|3[47][0-9]{13}|6(?:011|5[0-9]{2})[0-9]{12})$
```

---

## Regex Performance Tips

### ✅ DO

1. **Use specific patterns**
   ```regex
   # ✅ Good - specific
   \d{3}-\d{3}-\d{4}

   # ❌ Bad - too generic
   .*-.*-.*
   ```

2. **Anchor patterns**
   ```regex
   # ✅ Good - anchored
   ^https?:\/\/

   # ❌ Bad - searches entire string
   https?:\/\/
   ```

3. **Use non-capturing groups**
   ```regex
   # ✅ Good - non-capturing
   (?:https?):\/\/

   # ❌ Slower - capturing
   (https?):\/\/
   ```

### ❌ DON'T

1. **Avoid catastrophic backtracking**
   ```regex
   # ❌ DANGEROUS - exponential time!
   (a+)+b

   # ✅ Better
   a+b
   ```

2. **Don't use regex for nested structures**
   ```regex
   # ❌ BAD - Use HTML parser
   <div>(.*)</div>

   # ✅ Use DOMParser or cheerio instead
   ```

---

## Tools & Resources

### Online Regex Tools
- **[Regex Tester](https://orbit2x.com/regex-tester)** - Live testing with match highlighting
- **[Regex Library](https://orbit2x.com/regex-library)** - 40+ prebuilt patterns
- **[String Case Converter](https://orbit2x.com/string-case)** - Convert camelCase, snake_case, etc.
- **[Text Diff Tool](https://orbit2x.com/diff)** - Compare text with regex support

### Learning Resources
- **[Regex101](https://regex101.com/)** - Detailed explanations
- **[RegexOne](https://regexone.com/)** - Interactive tutorial
- **[MDN Regex Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)**

### Regex Testing Sites
- **[Orbit2x Regex Tester](https://orbit2x.com/regex-tester)** - Clean, fast UI
- **[Regex101](https://regex101.com/)** - Full explanation
- **[RegExr](https://regexr.com/)** - Visual tester

---

## FAQ

### Q: What's the difference between greedy and lazy quantifiers?
**A**:
- **Greedy** (`*`, `+`): Match as much as possible
- **Lazy** (`*?`, `+?`): Match as little as possible

```javascript
const html = "<div>foo</div><div>bar</div>";

// Greedy - matches entire string
html.match(/<div>.*<\/div>/)[0];
// "<div>foo</div><div>bar</div>"

// Lazy - matches first occurrence
html.match(/<div>.*?<\/div>/)[0];
// "<div>foo</div>"
```

### Q: How do I match newlines with `.`?
**A**: Use the `s` (dotall) flag:
```javascript
// Without s flag - doesn't match newlines
/line1.line2/.test("line1\nline2"); // false

// With s flag - matches newlines
/line1.line2/s.test("line1\nline2"); // true
```

### Q: What's the difference between `\w` and `[a-zA-Z0-9_]`?
**A**: They're equivalent in ASCII. `\w` also matches Unicode letters in some engines.

### Q: How do I escape special characters?
**A**: Use backslash `\`:
```regex
# Match literal dot
\.

# Match literal parentheses
\(\)

# Match literal backslash
\\
```

---

## Related Tools

- **[JSON Formatter](https://orbit2x.com/json-formatter)** - Format and validate JSON
- **[SQL Formatter](https://orbit2x.com/sql-formatter)** - Beautify SQL queries
- **[XML Formatter](https://orbit2x.com/xml-formatter)** - Format XML documents
- **[All Text Tools](https://orbit2x.com/tools)** - Complete text processing toolkit

---

**Made with ❤️ by [Orbit2x](https://orbit2x.com) - Free Developer Tools**

**Try now**: [Regex Tester](https://orbit2x.com/regex-tester) • [40+ Patterns](https://orbit2x.com/regex-library)
