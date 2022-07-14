import requests
import re
from operator import itemgetter
from bs4 import BeautifulSoup

import csv
import nltk
import numpy
nltk.download('punkt')
nltk.download('maxent_treebank_pos_tagger')


import re, time,csv
from selenium.webdriver.common.by import By
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC


url='http://www.uazone.com/gis/022098fedreg.txt'
headers={'User-Agent':'Mozilla/5.0 (Windows NT 6.1; rv:2.0.1) Gecko/20100101 Firefox/4.0.1'}


res=requests.get(url,headers=headers)
text=res.text
text=text.lower()
text=re.sub('[^a-z]',' ',text)
a=text.split(' ')
m={}
for v in a:
    if v in m: m[v]+=1
    else: m[v]=1
r=sorted(m.items(),key=itemgetter(1),reverse=True)
print(r)
