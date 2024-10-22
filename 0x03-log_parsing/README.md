0x03. Log Parsing - Project Description
This script processes log data from stdin, computing and displaying statistics. It reads the log line by line, tracks total file size, and counts occurrences of specific HTTP status codes.

Input Format:
The expected format for each log entry is:
<IP Address> - [<date>] "GET /projects/260 HTTP/1.1" <status code> <file size>
IP Address: The client’s IP address.
[date]: The timestamp of the request.
"GET /projects/260 HTTP/1.1": The HTTP method and resource being accessed.
<status code>: The HTTP response status code (an integer).
<file size>: The size of the response in bytes.
Any line that does not match this format will be ignored.

Output:
After processing every 10 lines, or if the script is interrupted (e.g., via CTRL + C), it outputs:

Total file size: The cumulative size of all valid responses.
Status code counts: A tally of each HTTP status code encountered.
Status Codes:
The script tracks and counts occurrences of the following HTTP status codes:

200: Success
301: Moved Permanently
400: Bad Request
401: Unauthorized
403: Forbidden
404: Not Found
405: Method Not Allowed
500: Internal Server Error
If a status code does not appear in the log or is invalid, it will not be included in the output.

Example Output:
yaml
Copy code
File size: 5213
200: 2
401: 1
403: 2
404: 1
405: 1
500: 3
File size: Cumulative file size of all valid entries.
Status codes: Number of occurrences, sorted by code.
Handling Errors:
Lines not matching the expected format are skipped.
When interrupted by CTRL + C, the script will print the current statistics and then exit.
