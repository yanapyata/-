import requests

TOKEN = '2619421814940190'

superheroes = ['Hulk', 'Captain America', 'Thanos']


def get_intellect():
    intelligence_dict = {}
    for hero in superheroes:
        url = f'https://www.superheroapi.com/api.php/{TOKEN}/search/{hero}'
        characteristics = requests.get(url).json()['results']
        for items in characteristics:
            if items['name'] in superheroes:
                intelligence_dict[items['name']] = int(items['powerstats']['intelligence'])
    max_intelligence = f' Самый умный супер-герой {max(intelligence_dict.keys())}, его интеллект равен {max(intelligence_dict.values())}'
    return max_intelligence


print(get_intellect())
