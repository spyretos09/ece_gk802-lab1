import requests


url = input("Enter the URL: ")      #Δώσε το url
r = requests.get(url)

print(f"Headers are: ,{r.headers} \n\n") #headers

print("a) Server: ",r.headers.get('Server'))

cookies = r.cookies
if cookies:                         #cookies κωδικας
    print("b) Cookies: yes ")
    for cookie in  r.cookies:
            print("Cookie name: ",cookie.name)
else:
    print("Not using Cookies !!!")