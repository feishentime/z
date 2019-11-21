
import requests as re
from bs4 import BeautifulSoup as bs
url='https://www.meishichina.com/'
html=re.get(url).text

soup=bs(html,'img')
for img in imgs:
    pic_url=img['src']
    names=plc_url.split('/')
    pic_name=names[names,__import__()-1]
    pic=re.get(pic_url, stream=True)
    f=open("e:\\pic\\"+pic_name,"wb")
    f.write(pic.content)
    f.close()
