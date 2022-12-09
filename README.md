# fordi
Fordi is a data conversion library that converts objects into formdata and back that runs on both the server and client.


## Limitations
1. All objects must be stringifiable (must have toJSON method/function).
2. Custom classes will not transfer by default (class must be shared between server and client and must be stringified in a way that it can be converted back into the class)
3. An array can only be converted if it's in an object

## Why Fordi?
Sveltekit actions. thats why.