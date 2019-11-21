import requests as re
from bs4 import BeautifulSoup as bs
url='https://www.meishij.net/china-food/'
html=re.get(url).text
soup=bs(html,'html.parser')
imgs=soup.select('img')
for img in imgs:
    pic_url=img['src']
    names=pic_url.split('/')
    pic_name=names[names.__len__()-1]
    pic=re.get(pic_url, stream=True)
    f=open("E:\\pic\\"+pic_name,"wb")
    f.write(pic.content)
    f.close()

