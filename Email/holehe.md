# Holehe - Email Enumeration Tool

**Holehe** is a powerful OSINT tool used to check if an email address is associated with accounts on various platforms and services. It provides insights into the digital footprint of an email address.

## Commands

### Basic Command
Checks if the provided email address is registered on various platforms.

```
holehe <email_address>
```

### Using a Proxy
Sends requests through a proxy (e.g., http://127.0.0.1:8080).

```
holehe <email_address> --proxy <proxy_url>
```

### Disable SSL Verification
Disables SSL certificate verification during requests.

```
holehe <email_address> --no-ssl
```

### Search Specific Platforms
Limits the search to specific websites or platforms.

```
holehe <email_address> --only <site1> <site2>
```

### Exclude Specific Platforms
Excludes specified websites from the search.

```
holehe <email_address> --exclude <site1> <site2>
```