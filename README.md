import requests

url = 'https://api.example.com/data'

headers = {
  'Authorization': 'Bearer MY_API_TOKEN'
}

params = {
  'limit': 50,
  'type': 'articles'  
}

response = requests.get(url, headers=headers, params=params)

if response.status_code == 200:
  data = response.json()
  for item in data['results']:
    print(item['title'])
else:
  print('Request failed with status code:', response.status_code)