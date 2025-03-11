import requests

url = 'https://api.example.com/data'

headers = {'Authorization': 'Bearer mytoken'}

params = {'category': 'sports', 'limit': 10}

response = requests.get(url, headers=headers, params=params)

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print('Request failed with status code:', response.status_code)