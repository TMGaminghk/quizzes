## Parse File
* The task is to parse a custom file into a data structure and print the result
* The custom file contain multiple lines of:
    + Empty line - ignore
    + “#” comment line - ignore
    + “XXX: abcd” - 0 or more tag lines where the “XXX” is the tag name; the “:” is separator; the “abcd” is tag value; both tag name and value should have head and tail space removed
    + CSV data - 0 or more lines of CSV (comma separated value); expect every line have the same number of separated values (or columns)
    + Repeat of all the above
    + Note: the sequence of the lines group are always: comment, tag and then csv
* Expect the program can handle basic errors (e.g. parse error, etc.)
* You may choose whatever programming language

**Example 1:**

*Input:*

```
# This is a comment
Name :      Day 1
Date:       2020-01-01
Content:    Environment Data
25.3°C,31.2°C,66.7%,sunny
24.1°C,30.7°C,66.7%,cloudy
...
# This is an other comment
Name :      Day 2
Date:       2020-01-02
Content :   Environment Data
24.3°C,29.9°C,66.7%,shower
25.6°C,30.3°C,66.7%,cloudy
...
```

*Output:*
```
Name: “Day 1”
Date: “2020-01-01”
Content: “Environment Data”
CsvData:
25.3°C,31.2°C,66.7%,sunny
24.1°C,30.7°C,66.7%,cloudy
...
Name: “Day 2”
Date: “2020-01-02”
Content: “Environment Data”
CsvData:
24.3°C,29.9°C,66.7%,shower
25.6°C,30.3°C,66.7%,cloudy
...

```
