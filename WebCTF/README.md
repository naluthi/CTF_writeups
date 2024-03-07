# CTF_writeups

## LEVEL 1:

Send an HTTP Request Using Curl
```md
curl http://127.0.0.1/80/
```

## LEVEL 4:

Set the host header in the HTTP Request using Curl
```md
curl -H "Host: 24f1044ffec9fb43bbdcdf6dfb29e3a4" http://127.0.0.1:80/
```

## LEVEL 7:

Set the PATH in the HTTP Request using Curl
```md
curl http://127.0.0.1:80/6de574eed75578d14f1407e856bd1e36
```

## LEVEL 10: 

URL Encode a PATH in an HTTP Request using Curl
```md
curl "http://127.0.0.1:80/15639efc%20f19688e2/90bd3c64%20238d4de4"
```

## LEVEL 13:

Specify an Argument in an HTTP Request using Curl
```md
curl "http://127.0.0.1:80/?a=26be464f58db5a42572dd2ada53ff229"
```

## LEVEL 16: 

Specify multiple arguments in an HTTP request using curl
```md
curl "http://127.0.0.1:80/?a=300cb73aaf31fc55cd4cb6b73abeea99&b=c8297c3f%2520172e2807%265d5839b4%2374ff496b"
```

## LEVEL 19: [POST]

Include form data in an HTTP request using curl
```md
curl -X POST "http://127.0.0.1:80/" -d "a=18df9dab9077717c9c68199c1cf8f29f"
```

## LEVEL 22: [POST]

Include form data with multiple fields in an HTTP request using curl
```md
curl -X POST "http://127.0.0.1:80/" -d "a=8d0f9321a81728159731d394b4042302" -d "b=26e37257%2075dd22a9%260127236a%23ebc4ee12"
```

## LEVEL 25: 

Include json data in an HTTP request using curl
```md
curl -X POST "http://127.0.0.1:80/" -H "Content-Type: application/json" -d '{"a": "3e1bf5fefe4de1571585569d2aefe184"}'
```

## LEVEL 28:

Include complex json data in an HTTP request using curl
```md
curl -X POST "http://127.0.0.1:80/" \
-H "Content-Type: application/json" \
-d '{
    "a": "e48c40c5e6080507ffb49fdcff158fca",
    "b": {
        "c": "ecc2e524",
        "d": ["b5b7c2c5", "a6597d18 a509e8e3&7db70cda#5781516b"]
    }
}'
```

## LEVEL 31:

Follow an HTTP redirect from HTTP response using curl
```md
curl http://127.0.0.1:80/
curl http://127.0.0.1:80/bd19e1c079cf40677409a034bb0a1de2
```

## LEVEL 34:

Include a cookie from HTTP response using curl
```md
curl -i http://127.0.0.1/
curl -b "cookie=1029b5a03c759d1febde8527a885e5f0" http://127.0.0.1:80/
```

## LEVEL 37:

Make an HTTP request using Curl, the server requires that you make 4 stateful requests

State: 1
```md
curl -c cookies.txt http://127.0.0.1:80/first
```

State: 2
```md
curl -b cookies.txt -c cookies.txt http://127.0.0.1:80/second
```

State: 3
```md
curl -b cookies.txt -c cookies.txt http://127.0.0.1:80/third
```

State: 4
```md
curl -b cookies.txt http://127.0.0.1:80/fourth
```
