# Code

## Syntax Highligting

```javascript title="test.js" linenums="0"
window.dataLayer = window.dataLayer || [];

function gtag() {
  dataLayer.push(arguments);
  console.log(window)
}

gtag('js', new Date());

gtag('config', 'UA-XXXXX');
```

```python title="bubble_sort.py" hl_lines="2 3 5"
def bubble_sort(items):
  for i in range(len(items)):
    for j in range(len(items) - 1 - i):
      if items[j] > items[j + 1]:
        items[j], items[j + 1] = items[j + 1], items[j]
```

```javascript title="return.js" hl_lines="2" linenums="0"
if (!test) {
  return null;
}
```

## Other Methods

## More
