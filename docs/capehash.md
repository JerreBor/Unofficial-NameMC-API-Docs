# NameMC Cape Hash API docs
NameMC has their own system for storing capes.

This API's purpose is to get a users NameMC Cape Hash.

### `GET /v1/namemc/capehash?username=:IGN_Here`
This is the only endpoint for this API.

Parameters are as follows:
- **`IGN_Here`** - the current username of the account

### Possible responses

The API will almost always return HTTP status code `200 OK` and set its `Content-Type` header to `application/json`.

If the user you provide doesn't exist, the API will return HTTP status code `404 Not Found`, and the `Content-Type` header will remain `application/json`.

Here are the different responses that can be returned:

**Returns the Cape Hash / HTTP `200`:**
```json
{"capehash":"cb5dd34bee340182"}
```

**No Cape / HTTP `200`:**
```json
{"capehash":null}
```

**You Didn't Provide The Username Parameter / HTTP `404`:**
```json
{"error":"You didn't supply an account to get a skin hash from! Add the parameter ?username=IGN_HERE."}
```

