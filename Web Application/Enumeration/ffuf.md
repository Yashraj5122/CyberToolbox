# FFUF (Fuzz Faster U Fool)

FFUF is a fast and flexible web fuzzing tool for discovering hidden files, directories, and parameters.

## Commands

### Basic Directory Fuzzing
To find hidden directories on a website, use the following command: 

```bash
ffuf -u http://example.com/FUZZ -w /path/to/wordlist.txt
```

### Fuzzing with Extensions
To search for specific file types like .php or .txt, append the -e flag:

```bash
ffuf -u http://example.com/FUZZ -w /path/to/wordlist.txt -e .php,.txt
```

### Parameter Discovery

To find hidden GET parameters, place FUZZ in the parameter position:
```bash
ffuf -u http://example.com/page.php?FUZZ=test -w /path/to/wordlist.txt
```

### POST Data Fuzzing
To fuzz POST data, specify the HTTP method using -X and the payload using -d:
```bash
ffuf -u http://example.com/login -w /path/to/wordlist.txt -X POST -d "username=FUZZ&password=pass"
```

### Custom Headers
Add custom headers like Authorization or Cookie:
```bash
ffuf -u http://example.com/FUZZ -w /path/to/wordlist.txt -H "Authorization: Bearer TOKEN"
```