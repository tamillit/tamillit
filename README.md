### Hi there 👋

import requests
from bs4 import BeautifulSoup

inp=input()
web= requests.get("https://ta.wiktionary.org/wiki/+inp")

data=web.content

soup=BeautifulSoup(data,features="html.parser")

tag=soup.find_all("ol","li")
a=1
for i in tag:
           print(a,".",i.text)
           a=a+1
