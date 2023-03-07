# curl

The curl command is used to transfer data to or from a server, using one of the
supported protocols (HTTP, HTTPS, FTP, FTPS, SCP, SFTP, TFTP, DICT, TELNET,
LDAP, or FILE). It is a versatile tool for accessing and manipulating data over
the internet.

## Usage:

```
curl [options] [URL]
```

- options modify the behavior of the curl command.
- URL is the address of the resource to be accessed or modified.

## Examples:

- Download a file from a URL.
  ```bash
  curl -O https://example.com/file.txt
  ```
- Download a file and save it with a different name.
  ```bash
  curl -o output.txt https://example.com/file.txt
  ```
- Display the HTTP headers of a response.
  ```bash
  curl -I https://example.com
  ```
- Send a POST request with data.
  ```bash
  curl -d 'param1=value1&param2=value2' -X POST https://example.com
  ```
- Send a request with a specific user agent.
  ```bash
  curl -A "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.36 Edge/16.16299" https://example.com
  ```
- Send a request with a specific referer.
  ```bash
  curl -e "https://google.com" https://example.com
  ```
- Follow redirects.
  ```bash
  curl -L https://example.com
  ```
- Use a proxy to connect to the server.
  ```bash
  curl -x http://proxy.example.com:8080 https://example.com
  ```
- Upload a file to a server.
  ```bash
  curl -F "file=@/path/to/local/file.txt" https://example.com/upload
  ```
- Download a file using FTP.
  ```bash
  curl -O ftp://example.com/file.txt
  ```
