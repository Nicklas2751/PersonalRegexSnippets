# MediathekView snippets

Some snippets i used for the MediathekView project

## Filer Crawler log
A snippet to filter normal lines "Durchsuche" wherer nothing happens between this normal line and the next.

### Example
Before:
```
.  Durchsuche: http://www.example.org/?id=idont&know=%C3%1
.  Durchsuche: http://www.example.org/?id=idont&know=%C3%2
.  Durchsuche: http://www.example.org/?id=idont&know=%C3%3
ERROR - Some random Text
.  Durchsuche: http://www.example.org/?id=idont&know=%C3%4
.  Durchsuche: http://www.example.org/?id=idont&know=%C3%5
```

After:
```
.  Durchsuche: http://www.example.org/?id=idont&know=%C3%3
ERROR - Some random Text
```

### Snippet
```
\.\s+Durchsuche:\s+[\w:/.?&=\-%]+\n\.\s*Durchsuche:\s[\w:/.?&=\-%]+
```
