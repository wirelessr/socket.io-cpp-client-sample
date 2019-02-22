# socket.io-cpp-client-sample
Sample of Socket.IO C++ Client.

This program provide result of command on native client's shell to web browser.

This program is explained in [linked Japanese article](http://llamerad-jp.hatenablog.com/entry/2015/05/22/151140).

## How to use.

### Compile native client.

```
$ git clone https://github.com/llamerada-jp/socket.io-cpp-client-sample.git
$ cd socket.io-cpp-client-sample
$ cd src
$ mkdir build
$ cd build
$ cmake -D SIO_DIR=<Socket.IO C++ Client dir> -D BOOST_ROOT=<Boost dir> ..
$ make
```

### Run server.

```
$ cd socket.io-cpp-client-sample
$ cd web
$ npm install
$ node index.js
```

### Run client

```
$ cd socket.io-cpp-client-sample
$ cd src/build
$ ./client http://localhost:8000/ <Your pc's ID.>
```

### Access by web browser.

Access to [http://localhost:8000/](http://localhost:8000/) and input browser's ID.
Input command (like 'ls') and push button.
The results on C++ client are displayed.

### Enable SSL

If you want to enable SSL on both server and client side, you can put `ENABLE_SSL` into cmake and node command line.

```
cmake -D ENABLE_SSL=1 -D SIO_DIR=<Socket.IO C++ Client dir> -D BOOST_ROOT=<Boost dir> ..
ENABLE_SSL=1 node index.js
```
