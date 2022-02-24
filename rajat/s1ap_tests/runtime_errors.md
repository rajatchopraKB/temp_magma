#### 1. requests.exceptions.ConnectionError: HTTPConnectionPool(host='192.168.60.142', port=3333): Max retries exceeded with url: /stats/switches (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f4a9e173da0>: Failed to establish a new connection: [Errno 111] Connection refused',))
Possible cause: the requred service is not running at port 3333\
Solution: restart magma services and wait for servicies to come up
```
sudo service magma@* stop
sudo service magma@magmad restart
sudo service magma@magmad status
```
