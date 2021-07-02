- 使用 brew 安装

  ```shell
  brew tap mongodb/brew
  brew install mongodb-community@4.4
  ```

  

- 启动/关闭 mongodb-community@4.4（background mode）

  ```shell
  brew services start mongodb/brew/mongodb-community
  
  brew services stop mongodb/brew/mongodb-community
  ```

  

- 启动 mongodb-community@4.4（session mode）

  ```shell
  mongod --config /opt/homebrew/etc/mongod.conf
  ```

- 进入 mongodb 数据库

  ```shell
  mongo
  ```

  得到一下信息

  ```shell
  MongoDB shell version v4.4.5
  connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
  Implicit session: session { "id" : UUID("198b26a2-7e63-4b14-a3fe-facbd39992b1") }
  MongoDB server version: 4.4.5
  Welcome to the MongoDB shell.
  For interactive help, type "help".
  For more comprehensive documentation, see
  	https://docs.mongodb.com/
  Questions? Try the MongoDB Developer Community Forums
  	https://community.mongodb.com
  ---
  The server generated these startup warnings when booting:
          2021-06-23T23:44:18.119+08:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
  ---
  ---
          Enable MongoDB's free cloud-based monitoring service, which will then receive and display
          metrics about your deployment (disk utilization, CPU, operation statistics, etc).
  
          The monitoring data will be available on a MongoDB website with a unique URL accessible to you
          and anyone you share the URL with. MongoDB may use this information to make product
          improvements and to suggest MongoDB products and deployment options to you.
  
          To enable free monitoring, run the following command: db.enableFreeMonitoring()
          To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
  ---
  ```

