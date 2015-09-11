Placeholder for developer documentation.

### Extracting csv data from the sqlite database

```
$ sqlite3 ActivityDatabase <<!
> .headers on
> .mode csv
> .output out.csv
> select * from GBActivitySamples;
> !
```

taken from [SO](http://stackoverflow.com/questions/5776660/export-from-sqlite-to-csv-using-shell-script).