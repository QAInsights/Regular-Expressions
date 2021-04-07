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

