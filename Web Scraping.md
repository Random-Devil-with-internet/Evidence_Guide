# Web Scraping
In week 7 I learned this time about web scraping which is gathering data using bots from the internet.

## BeautifulSoup
BeautifulSoup is a python package for extracting data from html and xml documents. It does this by making the html document into a parse tree sorting it into a hierarchical order of the html document.

How you use BeautifulSoup is by first using another python package Requests that will get the HTTP request to the website of the URL then you add the HEADERS variable to make the bot look like that it is a valid browser overwise the website might reject the bot. 

Then using BeautifulSoup you make the html document into a parse tree by using 'BeautifulSoup(page.content, "html.parser")'. The soup variable stores the tree parser of the html document. Next depending on what you want to extract from the html document I will for this evidence guide extract all of the links from a webpage. To do this you type 'link in' and after that you ues 'soup.find_all('a')' to find all the hyperlink tags in the html document. Then you loop though all of the hyperlink tags printing them in the terminal.

```python
import requests
from bs4 import BeautifulSoup

URL = "https://books.toscrape.com/"
HEADERS = {
    'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/66.0.3359.181 Safari/537.36',
    'Accept-Language': 'en-US, en;q=0.5'
}
page = requests.get(URL, headers=HEADERS, timeout=10)

soup = BeautifulSoup(page.content, "html.parser")
for link in soup.find_all('a'):
    print(link.get('href'))
```

## Selenium
Selenium is a python package for automating a web bowser which can be uesed to do repetitive and tedious tasks that a human would find boring, automate filling in forms and web Scraping.

## Reflection
