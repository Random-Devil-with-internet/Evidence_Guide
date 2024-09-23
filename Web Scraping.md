# Web Scraping
In week 7 I learned this time about web scraping which is gathering data using bots from the internet.

## BeautifulSoup
BeautifulSoup is a python package for extracting data from html and xml documents. It does this by making the html document into a parse tree sorting it into a hierarchical order of the html document.

How you use BeautifulSoup is by first using another python package Requests that will get the HTTP request to the website of the URL then you add the HEADERS variable to make the bot look like that it is a valid browser overwise the website might reject the bot. 

Then using BeautifulSoup you make the html document into a parse tree by using 'BeautifulSoup(page.content, "html.parser")'. The soup variable stores the tree parser of the html document. Next depending on what you want to extract from the html document I will for this evidence guide extract all of the links from a webpage. To do this you type 'link in' and after that you use 'soup.find_all('a')' to find all the hyperlink tags in the html document. Then you loop through all of the hyperlink tags printing them in the terminal.

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
Selenium is a python package for automating a web browser which can be used to do repetitive and tedious tasks that a human would find boring, automate filling in forms and web Scraping and other utilizations. To use selenium you first need to get a web driver Chrome, Firefox, Safari and Edge all work. Next you import the web driver by using this bit of code 'from selenium import webdriver'. Then you need to let the bot locate elements within the html document and you can also let it control the keys on your keyboard 'from selenium.webdriver.common.by import By'. To initialise the web driver you type 'driver = webdriver.Chrome()' or whatever web driver you are using. 

You then get the website that you want selenium to use and find the element in the html document. Then you print the element in the terminal by using a for loop.

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://www.wikipedia.org/")
link = driver.find_elements(By.TAG_NAME, 'a') 

for i in link: 
    print(i.text)
```

## Reflection
The skills that I have learned from web scrapping is the you can data and content form a website using a bot, you can automate a web browser which is helpfulll for automatically filling in forms, web scraping, repetitive tasks and functionality testing. Kowning these skills will assit me in the future especially if I get a job in IT. 

The ethical considerations of web scrapping are not to get people's private information without consnet eg. full name, email and phone number. Do not brech the terms of service of the website because they may ban web scrapping for over loading there server and higher costs of running a server. Robots.txt is a text file that is used to give guidelines to bots to tell them if they are allowed to web scrap the website or not and if alowed which bits of it.
