
#### 1. requests.exceptions.ConnectionError: HTTPConnectionPool(host='192.168.60.142', port=3333): Max retries exceeded with url: /stats/switches (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x7f4a9e173da0>: Failed to establish a new connection: [Errno 111] Connection refused',))
![Screenshot from 2022-02-24 17-53-57](https://user-images.githubusercontent.com/85698547/155525948-58f7a105-2458-4221-8cfc-17de9f2e1543.png)\
Possible cause: the requred service is not running at port 3333\
Solution: restart magma services and wait for servicies to come up
```
sudo service magma@* stop
sudo service magma@magmad restart
sudo service magma@magmad status
```
