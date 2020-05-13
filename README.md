# HTTPyng - The Python HTTP Ping Utility

Hi! This is HTTPynger. It is a very simple Python 3
script made to test connections to HTTP servers.
The program will make a request to a specific server
and count statistics, like the average response time, error rate, etc.
It was developed by Wesley Rodrigues <https://github.com/wesleyit>,
a guy with severe internet problems.

## Setup

This script has not been tested on Python 2, OK?
It was entirely written with built-in libraries, there is no need to
install dependencies. Just download it, give it execution permissions
and run!

You can clone the entire repo or just get the Python file at
<https://raw.githubusercontent.com/wesleyit/python_httpyng/master/httpyng>

### Installing and Using

```code
# Installing
$ wget https://raw.githubusercontent.com/wesleyit/python_httpyng/master/httpyng
--2020-05-13 19:00:16--  https://raw.githubusercontent.com/wesleyit/python_httpyng/master/httpyng
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 151.101.92.133
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|151.101.92.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3263 (3,2K) [text/plain]
Saving to: ‘httpyng’

httpyng                              100%[====================================================================>]   3,19K  --.-KB/s    in 0s

2020-05-13 19:00:17 (33,4 MB/s) - ‘httpyng’ saved [3263/3263]

$ chmod a+x httpyng
$ ./httpyng --help

usage: HTTPynger [-h] [-c COUNT] [-t TIMEOUT] [-u URL] [-a]

optional arguments:
  -h, --help            show this help message and exit
  -c COUNT, --count COUNT
                        Number of HTTPyngs to send.
  -t TIMEOUT, --timeout TIMEOUT
                        Timeout in seconds.
  -u URL, --url URL     URL to HTTPyng (with http:// or https://).
  -a, --about           Display the about message

# A perfect execution:
$ ./httpyng

Starting HTTPyng to http://www.google.com.br 10 times.
Press <CTRL>+<C> to exit.

------------------------------------------------------------------------

[000001] HTTPynging http://www.google.com.br, Resp: 200, Time: 1.656637663996662
[000002] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.12063869700068608
[000003] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.125455568995676
[000004] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.13121629499073606
[000005] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.14275436800380703
[000006] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.12244295301206876
[000007] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.1148413399932906
[000008] HTTPynging http://www.google.com.br, Resp: 200, Time: 2.2714427239989163
[000009] HTTPynging http://www.google.com.br, Resp: 200, Time: 1.0043731650075642
[000010] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.11556374300562311

------------------------------------------------------------------------

Finished running! Statistics:

Iterations: 10
Requests Ok: 10
Requests Bad 0
Success Rate: 100.0%
Fail Rate: 0.0%
Time Average: 0.5805366518005031 seconds
Time Min: 0.1148413399932906 seconds
Time Max: 2.2714427239989163 seconds

# An execution with failures:
$ ./httpyng

Starting HTTPyng to http://www.google.com.br 10 times.
Press <CTRL>+<C> to exit.

------------------------------------------------------------------------

[000001] HTTPynging http://www.google.com.br, Resp: 200, Time: 1.2714081519952742
[000002] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.1095878730120603
[000003] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.12243324800510891
[000004] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.1161000209976919
[000005] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.12693348398897797
[000006] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.11760112000047229
timed out
[000007] HTTPynging http://www.google.com.br, Resp: 500, Time: 3.68160566300503
[000008] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.11439314699964598
[000009] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.12580799500574358
[000010] HTTPynging http://www.google.com.br, Resp: 200, Time: 0.1257844589999877

------------------------------------------------------------------------

Finished running! Statistics:

Iterations: 10
Requests Ok: 9
Requests Bad 1
Success Rate: 90.0%
Fail Rate: 10.0%
Time Average: 0.5911655162009992 seconds
Time Min: 0.1095878730120603 seconds
Time Max: 3.68160566300503 seconds

```
