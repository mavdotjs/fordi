# fordi
Fordi is a data conversion library that converts objects into formdata and back.

Fordi can be used on both the server and the client.

## Limitations
1. All objects must be stringifiable.
2. Custom classes will not transfer by default
3. an array can only be converted if it's in an object