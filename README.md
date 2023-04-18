# xss-reflect-wordpress-cryptocurrency
XSS Stored in Plugin Cryptocurrency Widgets version - 2.6.2 - authenticated

Used WordPress version 6.2
Plugin Cryptocurrency Widgets version - 2.6.2

Access the Crypto Plugin menu and choose the "Add New Widget" option.

![image](https://user-images.githubusercontent.com/20262345/232639519-1a207ea1-a421-47bf-b32f-62a38f9bdea6.png)

Create a new widget with your title and inject the malicious XSS "PayLoad" of your choice.
In the example we are creating a title called "PoC2" with an XSS payload with just the alert message.


![image](https://user-images.githubusercontent.com/20262345/232640621-13046099-dffa-450f-8c3c-5e13d40475c9.png)

Request intercepted by Burp:
![image](https://user-images.githubusercontent.com/20262345/232640782-b9d18b85-48d4-43f8-81f6-fd81495ef7c7.png)


We can now access the page created from our "Widget":
http://127.0.0.1/?ccpw=poc2-alertxss-stored-cryptocurrency-widgets&preview=true

![image](https://user-images.githubusercontent.com/20262345/232641271-d7eac5ce-d9d8-4117-b4a7-01ca934d29ae.png)


Steal Cookies with Reflected XSS
If any exchange uses the Cryptocurrency Widgets version - 2.6.2 plugin, a malicious user can steal session cookies from authenticated users on the platform.


![image](https://user-images.githubusercontent.com/20262345/232642301-9c78fe5b-e606-474f-9642-54b1fe2fbba1.png)



