# jsonstorage-samples-python

## Create JSON:

```
import requests

url = "https://api.jsonstorage.net/v1/json?apiKey=<your api key>"
data = {'sender': 'Alice', 'receiver': 'Bob', 'temperature': 29, 'humidity': 67}

r = requests.post(url, json=data)

print(r.text)
print(r.status_code, r.reason)
````

## Update JSON:

```
import requests

url = "https://api.jsonstorage.net/v1/json/<userId>/<itemId>?apiKey=<your api key>"
data = {'sender': 'Alice', 'receiver': 'Bob', 'temperature': 29, 'humidity': 81}

r = requests.put(url, json=data)

print(r.text)
print(r.status_code, r.reason)
````

## Delete JSON:

```
import requests

url = "https://api.jsonstorage.net/v1/json/<itemId>?apiKey=<your api key>"
r = requests.delete(url)

print(r.text)
print(r.status_code, r.reason)

````
