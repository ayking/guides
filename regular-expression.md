Replace all lines which not contain `Text`
```
^((?!Text).)*$
```

Replace with Uppercase

```
(.*)
\U$1
```

Replace with first characte uppercase

```
(.)(.*)
\U$1$2
```
