# Swarm_Check-in_Data

926524 check-ins colleted from 3000 Swarm users  
Licensed under [Creative Commons Attribution Share Alike 4.0](http://choosealicense.com/licenses/cc-by-sa-4.0/).

## Description

We collected 1,562,452 check-ins from 5112 Swarm users with their consent, and randomly selected 3000 of them with 926524 check-ins at total for publicity.
The selected check-ins were generated in 3 cities, i.e., Hong Kong(HK), New York City(NYC), San Francisco(SFO).  
Respecting for users' privacy, we obscured the `user_id` field in the data.

## Files

- `hk.txt`: The check-ins generated in Hong Kong.
- `nyc.txt`: The check-ins generated in New York City.
- `sfo.txt`: The check-ins generated in San Francisco.

Each line in `.txt` files is a JSON object, representing for data of an user as follow:
```json
{
    "check-in_num":3,
    "local":0,
    "user_id":"123",
    "check-ins":[
        {
            "venue_category":"4bf58dd8d48988d1ed931735", 
            "venue_id":"4a7379d2f964a52088dc1fe3",
            "date":"2016-2-21",
            "time":"16:12:2",
            "lat":"22.3148321762",
            "lng":"113.9351031414"
        },
        {
            "venue_category":"4bf58dd8d48988d1f0931735",
            "venue_id":"4bef5da0d1b7d13a60bacdec",
            "date":"2016-1-31",
            "time":"7:13:9",
            "lat":"22.3137891166",
            "lng":"113.9338078331"
        },
        {
            "venue_category":"4bf58dd8d48988d1ed931735",
            "venue_id":"4a7379d2f964a52088dc1fe3",
            "date":"2016-1-31",
            "time":"6:40:36",
            "lat":"22.3148321762",
            "lng":"113.9351031414"
        }
    ]
}
```

Explanations for fields in JSON:

- `check-in_num`: the number of check-ins created by the user in the city
- `local`: whether the user is local to this city or not, 0 for nonlocal, 1 for local
- `user_id`: The user id has been obscured for privacy protection.
- `venue_category`: Refer to [https://developer.foursquare.com/categorytree](https://developer.foursquare.com/categorytree) for detail
- `venue_id` the check-in venue id in Swarm
- `date`: year-month-day
- `time`: hour:minute:second
- `lat`: the latitude at which the check-in is generated
- `lng`: the longitude at which the check-in is generated

### BibTex Entry
```
@inproceedings{lin2017understanding,
  title={Understanding user activity patterns of the Swarm app: a data-driven study},
  author={Lin, Shihan and Xie, Rong and Xie, Qinge and Zhao, Hao and Chen, Yang},
  booktitle={Proceedings of the 2017 ACM International Joint Conference on Pervasive and Ubiquitous Computing and Proceedings of the 2017 ACM International Symposium on Wearable Computers},
  pages={125--128},
  year={2017},
  organization={ACM}
}
```

