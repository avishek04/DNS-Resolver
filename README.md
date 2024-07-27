# Caching DNS Resolver
This project works like a basic DNS Resolver that caches the previously requested domain for a certain period of time for faster processing of the requests made for the same domain name. It uses Java's multi-threading feature to process mutiple requests parallelly.

Project Owner: Avishek Choudhury

## Tech Stack
* Java
* Multi-thread

## Implementation
1. Resolver receives and correctly decodes the DNS request from the client.
2. Resolver forwards requests to google when answers aren't in cache. Resolver decodes Google's response.
3. Resolver caches Google's responses and correctly evicts if their TTLs expire, expiration is detected when someone requests a stale record.
4. Resolver sends back properly formatted DNS responses to the client.
