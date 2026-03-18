# 🔤 Advanced String Manipulation – Regular Expressions in Python

> Part of the **ALX Africa Python** curriculum | `csfrost/Python`

---

## 📖 Overview

Regular expressions (regex) in Python are essential tools for anyone working with text data, enabling efficient searching, editing, and data manipulation. Mastering regex opens up a world of possibilities for data scientists and engineers, allowing for precise pattern matching and text processing in large datasets.

In this lesson, we explore Python's `re` library, focusing on practical applications such as extracting specific information and using compiled regex objects for performance. Topics covered include regex patterns, methods, and their use in real-world data processing challenges — especially when combined with **Pandas** for complex string operations.

---

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Understand the basics of Python's `re` library, including regex objects, character classes, and quantifiers for string pattern matching
- Utilise various regex methods for different pattern matching and string manipulation tasks
- Interpret and employ regex flags and basic pattern components effectively in Python
- Create and analyse complex regex patterns to efficiently extract and manipulate data
- Integrate regex with Pandas for advanced string operations within Python data structures


---

## 📂 Contents

```
Advanced_string_manipulation/
│
├── regex_basics.ipynb            # Regex objects, character classes, quantifiers
├── regex_methods.ipynb           # re.search, re.match, re.findall, re.sub, etc.
├── regex_flags_patterns.ipynb    # Flags (re.IGNORECASE, re.MULTILINE) and pattern components
├── complex_regex_patterns.ipynb  # Advanced extraction and manipulation patterns
└── pandas_string_operations.ipynb  # Integrating regex with Pandas str accessor
```

---

## 🧰 Key Concepts

### Regular Expressions (`re` module)

```python
import re

# Compile a regex pattern for reuse
pattern = re.compile(r'\d{3}-\d{4}')

# Search for a match
result = pattern.search("Call us at 012-3456 today")
print(result.group())  # Output: 012-3456
```

### Common Regex Methods

| Method | Description |
|---|---|
| `re.search()` | Finds the first match anywhere in the string |
| `re.match()` | Matches only at the beginning of the string |
| `re.findall()` | Returns a list of all non-overlapping matches |
| `re.sub()` | Replaces matches with a specified string |
| `re.split()` | Splits a string at each match |

### Character Classes & Quantifiers

| Symbol | Meaning |
|---|---|
| `\d` | Any digit (0–9) |
| `\w` | Any word character (a–z, A–Z, 0–9, _) |
| `\s` | Any whitespace character |
| `+` | One or more occurrences |
| `*` | Zero or more occurrences |
| `?` | Zero or one occurrence |
| `{n,m}` | Between n and m occurrences |

### Pandas String Operations with Regex

```python
import pandas as pd

df = pd.DataFrame({'email': ['user@example.com', 'admin@test.org', 'invalid-email']})

# Extract domain using regex
df['domain'] = df['email'].str.extract(r'@([\w.]+)')

# Filter rows matching a pattern
valid = df[df['email'].str.contains(r'^[\w.-]+@[\w.-]+\.\w+$', na=False)]
```

---

## 🔧 Requirements

- Python 3.x
- `pandas` library
- Jupyter Notebook (recommended)

Install dependencies:

```bash
pip install pandas jupyter
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/csfrost/Python.git

# Navigate to this lesson's folder
cd Python/Advanced_string_manipulation

# Launch Jupyter Notebook
jupyter notebook
```

---

## 📚 Resources

- [Python `re` module – Official Documentation](https://docs.python.org/3/library/re.html)
- [Pandas String Methods – Official Documentation](https://pandas.pydata.org/docs/user_guide/text.html)
- [Regex101 – Online Regex Tester](https://regex101.com/)
- [Regular Expressions HOWTO – Python Docs](https://docs.python.org/3/howto/regex.html)

---

## 👤 Author

**csfrost**

[![GitHub](https://img.shields.io/badge/GitHub-csfrost-181717?logo=github)](https://github.com/csfrost)

## 🙏 Acknowledgments

- [ALX Africa (ExploreAI Academy)](https://www.explore.ai/) — Course material and guidance

## 📄 License

This project is licensed under the [MIT License](./LICENSE).
