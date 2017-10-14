visql
===

Edit slices of SQL tables in vi.  Just specify a table and any filters
you want to apply, and the table will show up in vi in csv format.
Any edits you make will be applied back to the original source.

![demo](https://user-images.githubusercontent.com/118367/31579274-e3cc78b4-b100-11e7-88a2-63be8a358dbb.gif)

## Install

To edit local Sqlite databases, just do:

```
pip install visql
```

For PostgreSQL or MySQL support, add `catsql[postgres]` or `catsql[mysql]`:

```
pip install visql catsql[mysql]
pip install visql catsql[postgres]
```

For other databases, just install the appropriate [SQLAlchemy dialect](http://docs.sqlalchemy.org/en/latest/dialects/index.html).

## Use

```
visql test.sqlite3
visql test.sqlite3 --table users
visql postgres[ql]://user:pass@host/db --table users
visql mysql://user:pass@host/db --table users
visql test.sqlite3 --table users --grep paul
visql test.sqlite3 --table comments --sql "length(txt) < 40"
```

For all filters, see https://github.com/paulfitz/catsql#examples

