# Regular Expressions

## YouTube Playlist

📺 [https://www.youtube.com/playlist?list=PLJ9A48W0kpRLorIGHOM7g2OUsO2de3ERm](https://www.youtube.com/playlist?list=PLJ9A48W0kpRLorIGHOM7g2OUsO2de3ERm)

## Multiline Match with ?s

```
<title>(?s)(.+)<\/title>
```
In VS Code:  

```
<title>[\s\S\r]+</title>
```

## Multiline Mode in JMeter

```
<title>(?s)(.+?)<\/title>
```

## Find 36 characters

<id="32003b34-96f3-11eb-a8b3-0242ac130003">

```
id\=\"(.{36})\"
```

## Find how many products' prices

https://demostore.gatling.io/category/all  

```
<p>([\$][0-9]+\.[0-9]+)<\/p>
```
or
```
<p>\$((\d+)\.(\d+))<
```

## Find how many links

https://demostore.gatling.io/category/all

```
<a href="(.+?)"
```

```
href="\/category\/all\?page=\d"\s*class="page-link"\s*>\d<
```

## Find session id 

Lazy Quantifier : *?

Greedy Quantifier: *+?

```
jsessionid=(.+?)"
```

## Find response header values

```
content-encoding: (.*?)$
```

## URL Matching

```
(?i)petstore\.octoperf\.com(.*)
```

## Exact numbers matching

```
\b\d{5}\b
```
## JMESPath

Test String
```
{
    "id": 1,
    "type": "donut",
    "name": "Cake",
    "ppu": 0.55,

    "batters": {
        "batter": [
            {
                "id": 1001,
                "type": "Regular",
                "cal" : 10
            },
            {
                "id": 1002,
                "type": "Chocolate",
                "cal" : 100
            },
            {
                "id": 1003,
                "type": "Blueberry",
                "cal" : 5
            },
            {
                "id": 1004,
                "type": "Devil's Food",
                "cal" : 10
            }
        ]
    },
    "topping": [
        {
            "id": 5001,
            "type": "None"
        },
        {
            "id": 5002,
            "type": "Glazed"
        },
        {
            "id": 5005,
            "type": "Sugar"
        },
        {
            "id": 5007,
            "type": "Powdered Sugar"
        },
        {
            "id": 5006,
            "type": "Chocolate with Sprinkles"
        },
        {
            "id": 5003,
            "type": "Chocolate"
        },
        {
            "id": 5004,
            "type": "Maple"
        }
    ]
}
```

```
batters.batter[?id==`1001`]

length(batters.batter[*])

batters.batter[*].type | sort(@)

sort_by(batters.batter, &cal)[*].{Cal: cal}

batters.batter[*] | [*]

batters.batter[*].type | [?contains(@, 'Cho') == `true`]


sort_by(batters.batter, &cal)[*].{Cal: cal, id: id}

sort_by(batters.batter, &type)[*].{Cal: cal, id: id, type: type}
```

# CSS Selectors

Demo app: http://bank-of-anthos.xyz/home  
Ref: https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-last-child

## Extract title
```
head > title
```

## Extract Amount
```
#transaction-list > tr:nth-child(n) > td[class*=transaction-amount]
```
