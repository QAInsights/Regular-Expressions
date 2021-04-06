# Regular Expressions

## Multiline Mode in JMeter

```
<title>(?s)(.+?)<\/title>
```

## Find 36 characters

<id="32003b34-96f3-11eb-a8b3-0242ac130003">

```
id\=\"(.{36})\"
```

## Find how many products

https://demostore.gatling.io/category/all  

```
<p>[\$][0-9]+\.[0-9]+<\/p>
```

## Find how many links

https://demostore.gatling.io/category/all

```
<a href="(.+?)"
```

```
href="\/category\/all\?page=\d"\s*class="page-link"\s*>\d<
```

## Find jession 

Lazy Quantifier : *?

Greedy Quantifier: *+?

```
jsessionid=(.+?)"
```
