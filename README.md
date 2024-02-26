import requests

def main():
    url = input("Enter the URL: ") #Δώσε το url
    r = requests.get(url)
    
    print("a) Server: ",r.headers.get('Server'))

    cookies = r.headers.get('Get-Cookie')
    if cookies:
        print("b) Cookies: yes ")
        print("Cookie : ",cookies)
    else:
        print("Not using Cookies !!!")
 
if __name__ == "__main__":
    main()
