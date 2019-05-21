# Beautiful Soup Package for Python

## Import BeautifulSoup and Requests

```python
import requests
from bs4 import BeautifulSoup
```

## Make the Soup
```python
url = 'https://example.com'

page = requests.get(url)
soup = BeautifulSoup(page.text, 'html.parser')
```

## Find all instances of a tag

```python
for l in soup.find_all('a'):
    print(l)

## Prints all of the anchor tags found in the soup
```

## Get the 'href' element from all 'a' tags

```python
    for l in soup.find_all('a'):
        txt = l.get('href')
        print(txt)

## Prints all of the href paths found in the Soup
```