# urllib.parse Python Package

## Import

```python
from urllib.parse import urlparse, urljoin
```

## urlparse()

```python
url = "https://example.com/page?q=hi"

x = urlparse(url)
print(x)

> ParseResult(scheme='https', 
              netloc='example.com', 
              path='/page', 
              params='', 
              query='q=hi', 
              fragment='')
```

## urljoin()

```python
url = urljoin("https://example.com", "page")
print(url)
> https://example.com/page
```
