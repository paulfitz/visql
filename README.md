Edit SQL in vi.

```
pip install visql
pip install visql catsql[mysql]
pip install visql catsql[postgres]
```


```
visql test.sqlite3
visql test.sqlite3 --table users
visql postgres[ql]://user:pass@host/db
visql test.sqlite3 --table users --grep paul
```
