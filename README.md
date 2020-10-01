# webdevelopment
Web dev notes

Ping me if you want ant extra notes on any topic!
#a fun program to play with
import urllib.request,urllib.parse,urllib.error
import xml.etree.ElementTree as ET 
url=" http://py4e-data.dr-chuck.net/comments_382054.xml"
real=urllib.request.urlopen(url)
data=real.read().decode()
#print(data)
tree=ET.fromstring(data)
print(tree)
tags=tree.findall(".//comment")
su=0
for tag in tags:
    x=int(tag.find("count").text)
    su=su+x
print("sum =",su)    
