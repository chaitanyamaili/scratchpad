# HTTP Status Code Cheat Sheet

This cheat sheet lists HTTP status codes, grouped by their category, along with a brief explanation.

## 1xx - Informational Responses
These status codes indicate that the request was received and the process is continuing.

| Status Code | Name                    | Description                                                             |
|-------------|-------------------------|-------------------------------------------------------------------------|
| 100         | Continue                 | The client should continue with its request.                            |
| 101         | Switching Protocols      | The server is switching to a different protocol at the client’s request. |
| 102         | Processing (WebDAV)      | The server is processing the request but no response is available yet.   |

## 2xx - Success
Indicates that the request was successfully received, understood, and accepted.

| Status Code | Name                    | Description                                                             |
|-------------|-------------------------|-------------------------------------------------------------------------|
| 200         | OK                       | The request was successful, and the response contains the result.        |
| 201         | Created                  | The request was successful, and a resource was created.                  |
| 202         | Accepted                 | The request has been accepted for processing, but not yet completed.     |
| 203         | Non-Authoritative Info   | The information in the response is from a different source.              |
| 204         | No Content               | The request was successful, but there is no content to send in response. |
| 205         | Reset Content            | Tells the client to reset the document view.                             |
| 206         | Partial Content          | Only part of the resource was returned, due to a range header sent by the client. |

## 3xx - Redirection
Indicates that further action is required by the client to complete the request.

| Status Code | Name                    | Description                                                             |
|-------------|-------------------------|-------------------------------------------------------------------------|
| 300         | Multiple Choices         | The request has multiple possible responses.                            |
| 301         | Moved Permanently        | The requested resource has been moved to a new URI permanently.          |
| 302         | Found                    | The resource is temporarily located at a different URI.                  |
| 303         | See Other                | The client should retrieve the resource using a GET request.             |
| 304         | Not Modified             | The resource has not been modified since the last request.               |
| 307         | Temporary Redirect       | The request should be repeated with another URI; the same method will be used. |
| 308         | Permanent Redirect       | The resource has been permanently moved to another URI.                  |

## 4xx - Client Errors
Indicates that the client made an error, such as sending incorrect information.

| Status Code | Name                    | Description                                                             |
|-------------|-------------------------|-------------------------------------------------------------------------|
| 400         | Bad Request              | The request was invalid or cannot be processed by the server.            |
| 401         | Unauthorized             | Authentication is required and has failed or not yet been provided.      |
| 402         | Payment Required         | Reserved for future use (or for payment-related actions).                |
| 403         | Forbidden                | The server understands the request, but refuses to authorize it.         |
| 404         | Not Found                | The requested resource could not be found.                               |
| 405         | Method Not Allowed       | The request method is not supported by the resource.                     |
| 406         | Not Acceptable           | The requested resource is not available in a format acceptable to the client. |
| 407         | Proxy Authentication Required | The client must first authenticate with the proxy.                      |
| 408         | Request Timeout          | The server timed out waiting for the request.                            |
| 409         | Conflict                 | The request could not be completed due to a conflict with the current state of the resource. |
| 410         | Gone                     | The resource is no longer available at the server and no forwarding address is known. |
| 411         | Length Required          | The server requires the `Content-Length` header to be specified.         |
| 412         | Precondition Failed      | One or more conditions in the request header fields were false.          |
| 413         | Payload Too Large        | The request is larger than the server is willing or able to process.     |
| 414         | URI Too Long             | The URI provided was too long for the server to process.                 |
| 415         | Unsupported Media Type   | The media type of the request is not supported by the server.            |
| 416         | Range Not Satisfiable    | The range specified by the `Range` header field cannot be fulfilled.     |
| 417         | Expectation Failed       | The server cannot meet the expectations set by the `Expect` request header. |
| 418         | I'm a teapot             | An April Fools' joke from 1998 (RFC 2324).                               |
| 422         | Unprocessable Entity     | The request is well-formed, but was unable to be followed due to semantic errors (WebDAV). |
| 426         | Upgrade Required         | The server requires the client to upgrade to a different protocol.       |
| 429         | Too Many Requests        | The client has sent too many requests in a given period.                 |

## 5xx - Server Errors
Indicates that the server failed to fulfill a valid request.

| Status Code | Name                    | Description                                                             |
|-------------|-------------------------|-------------------------------------------------------------------------|
| 500         | Internal Server Error    | The server encountered an unexpected condition that prevented it from fulfilling the request. |
| 501         | Not Implemented          | The server does not support the functionality required to fulfill the request. |
| 502         | Bad Gateway              | The server received an invalid response from the upstream server.        |
| 503         | Service Unavailable      | The server is currently unable to handle the request due to temporary overload or maintenance. |
| 504         | Gateway Timeout          | The server, acting as a gateway, timed out waiting for a response from the upstream server. |
| 505         | HTTP Version Not Supported | The server does not support the HTTP version used in the request.      |
| 507         | Insufficient Storage     | The server cannot store the representation needed to complete the request (WebDAV). |
| 511         | Network Authentication Required | The client needs to authenticate to gain network access.            |

---

### Notes:
- This list covers the most common HTTP status codes. Some status codes (especially in the 4xx and 5xx ranges) may be less frequently encountered.
- Status codes like `418 I'm a teapot` are used for humorous purposes or edge cases.

---

Feel free to copy this content into your Markdown file and make adjustments as needed!
