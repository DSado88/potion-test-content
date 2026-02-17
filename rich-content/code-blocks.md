# Code Block Tests

## JavaScript

```javascript
function fibonacci(n) {
  if (n <= 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

// Arrow function variant
const fib = (n) => n <= 1 ? n : fib(n - 1) + fib(n - 2);

console.log(fibonacci(10)); // 55
```

## Python

```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)

print(quicksort([3, 6, 8, 10, 1, 2, 1]))
```

## Rust

```rust
use std::collections::HashMap;

fn word_count(text: &str) -> HashMap<&str, usize> {
    let mut counts = HashMap::new();
    for word in text.split_whitespace() {
        *counts.entry(word).or_insert(0) += 1;
    }
    counts
}

fn main() {
    let counts = word_count("hello world hello rust world");
    println!("{:?}", counts);
}
```

## Shell

```bash
#!/bin/bash
set -euo pipefail

for file in *.md; do
  echo "Processing: $file"
  wc -l "$file"
done | sort -rn | head -10
```

## JSON

```json
{
  "name": "potion-test",
  "version": "1.0.0",
  "dependencies": {
    "react": "^19.0.0",
    "next": "^16.0.0"
  },
  "scripts": {
    "dev": "next dev",
    "build": "next build"
  }
}
```

## No Language Specified

```
This is a code block
with no language specified.
It should render as plain text.
```

## Inline Code vs Block

Use `npm install` to install dependencies.

```
npm install
```

## Code with Very Long Lines

```
This is a very long line that should probably scroll horizontally rather than wrap because code blocks typically preserve whitespace and line formatting exactly as written without any word wrapping at all even when the line extends far beyond the visible viewport area.
```

## Code with Special Characters

```html
<div class="container">
  <p>Hello &amp; welcome!</p>
  <script>alert('XSS test: <script>bad</script>');</script>
  <!-- Comment with "quotes" and 'apostrophes' -->
</div>
```

## Empty Code Block

```
```

## Code Block with Tabs

```
Level 0
	Level 1 (tab)
		Level 2 (two tabs)
			Level 3 (three tabs)
```

## Diff

```diff
- const old = "removed line";
+ const new = "added line";
  const unchanged = "same";
```

## YAML

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: potion
  labels:
    app: potion
spec:
  replicas: 3
  selector:
    matchLabels:
      app: potion
```

## SQL

```sql
SELECT u.name, COUNT(o.id) as order_count
FROM users u
LEFT JOIN orders o ON u.id = o.user_id
WHERE u.created_at > '2025-01-01'
GROUP BY u.name
HAVING COUNT(o.id) > 5
ORDER BY order_count DESC
LIMIT 10;
```
