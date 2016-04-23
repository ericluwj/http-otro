# http-otro

A configuration lib and caller for [isomorphic-fetch](https://github.com/matthew-andrews/isomorphic-fetch):

```
import http from 'http-otro'
import { fetch } from 'isomorphic-fetch'

http({host: 'myhost', headers: {'Authorization': 'Bearer SomeToken'}}).get('/foo', {bar: 'baz'}) // Requests GET /foo?bar=baz
.then((res)=>{
  //deal with response
})
```

Default `host` and `headers` can be provided via `http`, or you can just call `http().method`.

For all methods, headers can be given via the last param. A `Content-Type` of `application/json` is the default for all requests.

# API

## request(resource, method, body={}, headers={})

All other methods alias this method.

## get(resource, params={}, headers={})

Turns `params` into a query string.

## post(resource, body={}, headers={})

## put(resource, body={}, headers={})

## del(resource, body={}, headers={})
