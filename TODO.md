1. Figure out how to recursively convert data
2. Figure out how to parse the converted data (maybe with peggy.js)


# Conversion
```json
{
    "data": ["abc", 123, true],
    "{stuff}": {
        "data": 123,
        "nest": {
            "data": "world"
        }
    }
}
```
Converts to:
```
{data}
array

data[0]
str:(abc)

data[1]
num:(123)

data[2]
bool:(1)

// url encoded name
{%7Bstuff%7D}
object

%7Bstuff%7D[str:(data)]
num:(123)

{%7Bstuff%7D[str:(nest)]}
object

%7Bstuff%7D[str:(nest)][str:(data)]
str:(hello)
```