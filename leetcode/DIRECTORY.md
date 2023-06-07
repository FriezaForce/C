Traceback (most recent call last):
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/connectionpool.py", line 536, in _make_request
    response = conn.getresponse()
               ^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/connection.py", line 454, in getresponse
    httplib_response = super().getresponse()
                       ^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/http/client.py", line 1375, in getresponse
    response.begin()
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/http/client.py", line 318, in begin
    version, status, reason = self._read_status()
                              ^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/http/client.py", line 279, in _read_status
    line = str(self.fp.readline(_MAXLINE + 1), "iso-8859-1")
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/socket.py", line 706, in readinto
    return self._sock.recv_into(b)
           ^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/ssl.py", line 1278, in recv_into
    return self.read(nbytes, buffer)
           ^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/ssl.py", line 1134, in read
    return self._sslobj.read(len, buffer)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TimeoutError: The read operation timed out

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/requests/adapters.py", line 486, in send
    resp = conn.urlopen(
           ^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/connectionpool.py", line 844, in urlopen
    retries = retries.increment(
              ^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/util/retry.py", line 470, in increment
    raise reraise(type(error), error, _stacktrace)
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/util/util.py", line 39, in reraise
    raise value
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/connectionpool.py", line 790, in urlopen
    response = self._make_request(
               ^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/connectionpool.py", line 538, in _make_request
    self._raise_timeout(err=e, url=url, timeout_value=read_timeout)
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/urllib3/connectionpool.py", line 370, in _raise_timeout
    raise ReadTimeoutError(
urllib3.exceptions.ReadTimeoutError: HTTPSConnectionPool(host='leetcode.com', port=443): Read timed out. (read timeout=10)

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/home/runner/work/C/C/scripts/leetcode_directory_md.py", line 123, in <module>
    tasks_list = fetch_leetcode_folder_tasks(solutions_folder)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/runner/work/C/C/scripts/leetcode_directory_md.py", line 24, in fetch_leetcode_folder_tasks
    resp = requests.get("https://leetcode.com/api/problems/algorithms/", timeout=10)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/requests/api.py", line 73, in get
    return request("get", url, params=params, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/requests/api.py", line 59, in request
    return session.request(method=method, url=url, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/requests/sessions.py", line 589, in request
    resp = self.send(prep, **send_kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/requests/sessions.py", line 703, in send
    r = adapter.send(request, **kwargs)
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.11.3/x64/lib/python3.11/site-packages/requests/adapters.py", line 532, in send
    raise ReadTimeout(e, request=request)
requests.exceptions.ReadTimeout: HTTPSConnectionPool(host='leetcode.com', port=443): Read timed out. (read timeout=10)
