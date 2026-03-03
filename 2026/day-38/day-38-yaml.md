## Files Created
- person.yaml
- server.yaml

---

## Task 1: Key-Value Pairs
I created person.yaml with basic key-value pairs.
I verified it using `cat person.yaml` and ensured:
- No tabs
- Clean indentation
- Correct boolean usage

---

## Task 2: Lists
I added lists using:
1. Block style
2. Inline style

### Two ways to write lists in YAML:
- Block list using `-`
- Inline list using `[item1, item2]`

---

## Task 3: Nested Objects
I learned that YAML hierarchy depends completely on indentation.

Adding a tab instead of spaces caused validation to fail.

---

## Task 4: Multi-line Strings

### `|`
- Preserves newlines
- Used for scripts and config files

### `>`
- Folds lines into a single line
- Used for long text or descriptions

---

## Task 5: Validation
I validated both files using yamllint.
Breaking indentation resulted in errors like:
- `mapping values are not allowed here`
- `bad indentation`

After fixing spacing, validation passed.

---

## Task 6: Spot the Difference

### What’s wrong with Block 2?
- `tools` list is not properly indented
- `- docker` should be on the next indented line

Correct indentation is mandatory in YAML.

---

## What I Learned (Key Takeaways)
1. YAML uses **spaces only — never tabs**
2. Indentation defines structure
3. Validation tools save time and prevent CI/CD failures

---

## Aha Moment 💡
A single tab can break an entire pipeline 😅  
Always validate YAML before committing!