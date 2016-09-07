# jsonparse
A JSON parser implementation *mostly* written in pure bash

## Usage

```bash
cat sample.json
# {
#   "foo": 42,
#   "bar": [
#     {
#       "baz": "Hello World"
#     },
#     false
#   ]
# }

cat sample.json | ./jsonparse foo
# 42

cat sample.json | ./jsonparse bar
# [{"baz":"Hello World"},false]

./jsonparse 'bar[0].baz' < sample.json
# Hello World
```
